+++
title = "Backend"
weight = 1
+++

## Local Backend Setup

To start the local setup of the application the backend needs to be fully operational first. This includes not only the backend itself, providing websockets for the dashboard and APIs for the dashboard, admin console and mobile app, but also the dependencies which the backend requires.

The KatApp backend has some [documentation](https://apidoc.katapp.org/) guiding new users through a simplified setup for the backend. The easiest way to set up the Backend is using Docker:

```
docker-compose up
```

This will set up the service and all of its required dependencies.

Note: If the initial build of the backend container fails be sure to add aws credentials into the .aws folder in your users directory. The .aws folder is required for the dev container setup to run successfully.

It is recommended to run the system locally using MongoDB. This is done automatically when using docker-compose. Once the backend and its dependencies are fully operational the *createInitialUser.sh* script, which can be found in the *scripts* directory of the *katapp-backend* repository, can be ran. This will automatically create an admin user with all neccessary permissions to operate the Tenant Admin Console and Dashboard locally. The default login for this user is the same across both the Dashboard and Tenant Admin Console:

* local@katapp.org
* @Local123

The credentials can be adjusted in the script.

### Viewing saved data

The local backend uses MongoDB, unless specified otherwise. The database and neccessary tables are created at runtime whenever needed. You can check the saved data using the [MongoDB Compass](https://www.mongodb.com/products/tools/compass). Run the application and connect to the default port provided at startup to get started. If the script has already been ran or data has already been saved in other ways, the KatApp database should have been created by the database. You can view its collections and saved data from here.