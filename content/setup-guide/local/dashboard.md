+++
title = "Dashboard"
weight = 2
+++

## Local Dashboard Setup

To test the Dashboard locally the Backend needs to be fully operational. To set up the Dashboard to run on the local backend the .env file in the root directory of the project needs to be edited. The following fields need to be modified for local testing:

* VITE_APP_BACKEND_WEBSOCKET_URL=ws://localhost:9998
* VITE_APP_BACKEND_BASE_URL=http://localhost:9997

The Dashboard can be started locally using the included docker files by running:

```
docker-compose up
```

This will make the Dashboard available at http://localhost:3000.

Alternatively, to run the dashboard outside of a container [Node.js](https://nodejs.org/en) needs to be installed. Once Node.js is installed run the following commands in the projects root directory:

```
npm i -g yarn
yarn
yarn start
```

This will start a development server which listens for changes in the projects root directory and displays the current version of your project at http://localhost:3000.