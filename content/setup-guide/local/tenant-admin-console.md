+++
title = "Admin Console"
weight = 3
+++

## Local Admin Console Setup

The Tenant Admin Console is set up very similarly to the Dashboard. To run it using the local backend create an .env.local file in the root directory of the project. In it define the following environment variables:

* VITE_APP_BACKEND_BASE_URL=http://localhost:9997/v1

The Tenant Admin Console can be started locally using the included docker container by running:

```
docker-compose up
```

This will make the Tenant Admin Console available at http://localhost:3001.

Alternatively, to run the Tenant Admin Console outside of a container [Node.js](https://nodejs.org/en) needs to be installed. Once Node.js is installed run the following commands in the projects root directory:

```
npm i -g yarn
yarn
yarn start
```

This will start a development server which listens for changes in the projects root directory and displays the current version of your project at http://localhost:3000.