## **Personal Activity Project**

At first it needs to install **backend** and **frontend** subprojects:

> git submodule init

### _Frontend:_

> **build:**

`cd frontend`

`npm run build`

> **develop with WebpackDevServer:**

`cd frontend`

`npm start`

### _Database:_

- create **db** directory _(for database file system containing)_
- add **db.env** file which contains Postgress ENV variables _(NodeJS application and Postgress container will use it together for create connection between application and database)_:
  - PGPASSWORD=qwerty
  - PGUSER=somebody
  - PGDATABASE=mydb
  - PGHOST=**db** ! _this name of host is important, it equals to service name in Docker-Compose configuration_

### _Backend:_

> **Build application**

`docker-compose -f app.yml build`

> **Run application**

`docker-compose -f app.yml up`

> **Stop application and network**

`docker-compose -f app.yml down`

> **Backend TypeScript transpilation:**

`cd backend`

`npm run watch-ts`

## **Also Adminer (DB management) will be able to use on [localhost:5000](localhost:5000) after docker-compose was starting**
