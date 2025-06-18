+++
title = "Admin Console"
weight = 3
+++

## Local Admin Console Setup

### Prerequisites

- Backend must be running locally
- Node.js (for non-Docker setup)

### Configuration

Create `.env.local` in the project root:
```env
VITE_APP_BACKEND_BASE_URL=http://localhost:9997/v1
```

### Running the Admin Console

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

The admin console will be available at http://localhost:3001. In development mode, it automatically reloads when you make changes.