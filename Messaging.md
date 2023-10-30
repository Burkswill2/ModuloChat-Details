## Messaging Protocol

Real-time messaging uses WebSockets for bidirectional communication between clients and servers. 

### Connecting

1. Client sends WebSocket connection request to server. 

2. Server accepts connection, assigns user ID and room ID if provided.

3. Server sends `connect_success` event to client with user ID and room ID.

### Joining Rooms

1. Client sends `join_room` event with room ID to join a chat room.

2. Server verifies room access and sends `room_joined` event on success, else `room_join_error`.

3. Server broadcasts `user_joined` event to all connected room members.

### Sending Messages 

1. Client sends `new_message` event with room ID, text content, and metadata. 

2. Server broadcasts `message_received` event to all room members with message payload.

3. Server updates message status to `sent`.

4. Recipient clients update read status via `message_read` events.

### Presence Updates

- Server sends real-time `user_joined` and `user_left` events as users enter or leave rooms.

- Clients display active user list based on presence events.

### Reconnection Logic

- Clients attempt to reconnect on lost connections and re-join rooms. 

- Server resumes prior state/rooms on reconnect.
