# ModuloChat Environment Setup

This comprehensive guide covers setting up local development environments for ModuloChat.

## Operating Systems

- [macOS](https://www.apple.com/macos/) 
- [Linux (Ubuntu)](https://ubuntu.com/)
- [Windows 10/11](https://www.microsoft.com/en-us/windows) 

Windows may require additional installation steps.

## Core Tools

- [Git](https://git-scm.com/) (v2.30+): `brew install git` 
- [Docker Desktop](https://www.docker.com/products/docker-desktop): `brew install --cask docker`
- [Docker Compose](https://docs.docker.com/compose/): `pip install docker-compose`
- [Node.js](https://nodejs.org/) (v14+ LTS): `brew install node` 
- [Yarn](https://yarnpkg.com/) (v1.22+): `npm install -g yarn`

## IDEs & Code Editors

- [WebStorm](https://www.jetbrains.com/webstorm/): JavaScript IDE
- [IntelliJ IDEA](https://www.jetbrains.com/idea/): Java IDE 
- [PyCharm](https://www.jetbrains.com/pycharm/): Python IDE
- [RubyMine](https://www.jetbrains.com/ruby/): Ruby IDE
- [Xcode](https://developer.apple.com/xcode/): `brew install --cask xcode`
- [Android Studio](https://developer.android.com/studio): Android IDE
- [VS Code](https://code.visualstudio.com/): `brew install --cask visual-studio-code`

## Frontend Development

### React

Install React:

```
npx create-react-app my-app
cd my-app
yarn add react-router-dom redux
```

### Vue

Install Vue:

```
yarn global add @vue/cli
vue create my-app
cd my-app
vue add router
```

### Angular

Install Angular:

```
yarn global add @angular/cli
ng new my-app
cd my-app
```

## Backend Development

See READMEs in each backend repo for setup:

- [backend-java](https://github.com/Burkswill2)
- [backend-python](https://github.com/Burkswill2)
- [backend-c++](https://github.com/Burkswill2)
- [backend-swift](https://github.com/Burkswill2)
- [backend-kotlin](https://github.com/Burkswill2)
- [backend-Ruby](https://github.com/Burkswill2)
    

## Databases 

Run locally using Docker:

```
docker run -d -p 5432:5432 postgres 
docker run -d -p 27017:27017 mongo
docker run -d -p 6379:6379 redis
```


- **PostgreSQL** - This open source relational database would be used as the primary persistent data store. Things like message history, user accounts, room data, etc. would reside here.

- **MongoDB** - A document-based NoSQL database that can handle more unstructured or polymorphic data if needed. Could be used in conjunction with Postgres.

- **Redis** - An in-memory data store used for caching and message queuing. So caching frequently accessed data from Postgres and also for real-time messaging via pub/sub channels.

- **Docker** - Used to containerize and run all the database systems above (Postgres, MongoDB, Redis) in an isolated, reproducible way during development.


## Infrastructure

- [Kubernetes](https://kubernetes.io/)
- [Prometheus](https://prometheus.io/), [Grafana](https://grafana.com/)
- [ELK Stack](https://www.elastic.co/what-is/elk-stack)
- [GitHub Actions](https://github.com/features/actions)
