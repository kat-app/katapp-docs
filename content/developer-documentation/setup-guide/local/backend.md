+++
title = "Backend"
weight = 1
+++

## Local Backend Setup

The backend provides websockets for the dashboard and APIs for the dashboard, admin console, and mobile app. Follow these steps to get it running:

### Quick Start

```bash
docker-compose up
```

This sets up the backend and all dependencies automatically.

### Prerequisites

- AWS credentials in `~/.aws/` directory (required for dev container setup)
- MongoDB (automatically configured with docker-compose)

### Initial Setup

1. Run the backend using docker-compose
2. Execute `createInitialUser.sh` from the `scripts` directory in `katapp-backend` repository
3. This creates an admin user with full permissions for both Tenant Admin Console and Dashboard

Default credentials:
- Email: local@katapp.org
- Password: @Local123

You can modify these credentials in the script.

### Database Access

The backend uses MongoDB by default. To view the data:
1. Install [MongoDB Compass](https://www.mongodb.com/products/tools/compass)
2. Connect using the port shown at startup
3. The `KatApp` database and collections will be created automatically when data is saved

For detailed API documentation, visit [apidoc.katapp.org](https://apidoc.katapp.org/).