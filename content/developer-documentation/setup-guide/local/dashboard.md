+++
title = "Dashboard"
weight = 2
+++

## Local Dashboard Setup

### Prerequisites

- Backend must be running locally
- Node.js (for non-Docker setup)

### Configuration

Update `.env` in the project root:
```env
VITE_APP_BACKEND_WEBSOCKET_URL=ws://localhost:9998
VITE_APP_BACKEND_BASE_URL=http://localhost:9997
```

### Running the Dashboard

#### Option 1: Docker

```bash
docker-compose up
```

#### Option 2: Local Development

```bash
npm i -g yarn
yarn
yarn start
```

The dashboard will be available at http://localhost:3000. In development mode, it automatically reloads when you make changes.