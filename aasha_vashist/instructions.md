# Fenrir Online Gaming Website - Instructions

## Project Overview
Fenrir is a full-stack online gaming platform built with modern web technologies.

## Prerequisites
- Node.js v18+ and npm v9+
- PostgreSQL 14+
- Redis 6+
- Docker (optional, for containerized setup)

## Local Development Setup

### 1. Clone the Repository
```bash
git clone https://github.com/aasha-vashist/fenrir-gaming.git
cd fenrir-gaming
```

### 2. Environment Configuration
Copy the example environment file and update the values:
```bash
cp .env.example .env
```
Key variables to configure:
- `DATABASE_URL` - PostgreSQL connection string
- `REDIS_URL` - Redis connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `AWS_ACCESS_KEY_ID` / `AWS_SECRET_ACCESS_KEY` - AWS credentials

### 3. Install Dependencies
```bash
npm install
```

### 4. Database Setup
```bash
npm run db:migrate
npm run db:seed
```

### 5. Start Development Servers
```bash
# Terminal 1 - Backend API
npm run dev:server

# Terminal 2 - Frontend
npm run dev:client

# Terminal 3 - WebSocket server
npm run dev:ws
```

### 6. Access the Application
- Frontend: http://localhost:3000
- API: http://localhost:4000/api
- API Docs: http://localhost:4000/docs

## Available Scripts
| Command | Description |
|---------|-------------|
| `npm run dev` | Start all dev servers concurrently |
| `npm run build` | Production build |
| `npm test` | Run test suite |
| `npm run lint` | Lint codebase |
| `npm run format` | Format code with Prettier |

## Deployment
```bash
# Build for production
npm run build

# Deploy to AWS (requires configured AWS CLI)
npm run deploy
```

## Project Structure
```
fenrir-gaming/
├── client/          # React frontend
├── server/          # Express API server
├── ws/              # WebSocket server
├── shared/          # Shared types and utilities
├── docs/            # Documentation
└── infra/           # Infrastructure as code
```
