# Test Task Master 📝

A modern, full-stack article management system built with NestJS and PostgreSQL, featuring clean architecture and a Swagger API.

## 🔗 Links

[![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)](https://nestjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)](https://www.prisma.io/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)](https://swagger.io/)

## ✨ Features

- 🚀 High-performance NestJS backend
- 🧩 TypeScript for type safety
- 📊 PostgreSQL database for reliable data storage
- 🔄 Complete article CRUD operations
- 📚 Prisma ORM for database management
- 📝 Swagger API documentation
- 🧪 Comprehensive testing suite
- 🔥 Hot reload development environment
- 🐳 Containerized with Docker and Docker Compose
- 🔒 Environment-based configuration
- ⚡ Fast and efficient database migrations

## 🛠️ Tech Stack

### Backend
- **Framework**: NestJS
- **Language**: TypeScript
- **Database**: PostgreSQL
- **ORM**: Prisma
- **API Documentation**: Swagger
- **Testing**: Jest
- **Environment**: Node.js

### DevOps & Infrastructure
- **Containerization**: Docker with multi-stage builds
- **Container Orchestration**: Docker Compose
- **Environment Management**: dotenv

### Development Tools
- **Code Style**: ESLint, Prettier
- **API Testing**: Jest test suite
- **Hot Reload**: NestJS watch mode

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Docker and Docker Compose (for containerized deployment)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/article-flux.git
cd article-flux
```

2. Install dependencies:
```bash
yarn install
```

3. Set up environment variables:
```bash
# Create a .env file with the following content
DATABASE_URL="postgresql://postgres:postgres@localhost:5432/article-flux?schema=public"
```

4. Generate Prisma client and run migrations:
```bash
yarn prisma:generate
yarn prisma:migration
```

5. Seed the database (optional):
```bash
yarn prisma:seed
```

6. Start the development server:
```bash
yarn start:dev
```

7. Access the Swagger API documentation:
```
http://localhost:3000/api
```

## 📁 Project Structure

```
article-flux/
├── prisma/                    # Prisma ORM configuration
│   ├── migrations/           # Database migrations
│   ├── schema.prisma         # Database schema definition
│   └── seed.ts               # Database seeding script
├── src/                       # Application source code
│   ├── articles/             # Articles module
│   │   ├── dto/              # Data Transfer Objects
│   │   ├── entities/         # Entity definitions
│   │   ├── articles.controller.ts   # API endpoints
│   │   └── articles.service.ts      # Business logic
│   ├── prisma/               # Prisma service
│   ├── app.module.ts         # Main application module
│   └── main.ts               # Application entry point
├── test/                      # End-to-end tests
├── Dockerfile                 # Docker configuration
├── docker-compose.yml         # Docker Compose configuration
└── package.json               # Project dependencies and scripts
```

## 🔧 Development

### Local Development
```bash
# Development with hot reload
yarn start:dev

# Debug mode
yarn start:debug

# Production mode
yarn start:prod
```

### Docker Development
```bash
# Build and run with Docker Compose
docker-compose up -d
```

## 🧪 Testing

```bash
# Run unit tests
yarn test

# Run tests with coverage
yarn test:cov

# Run end-to-end tests
yarn test:e2e
```

### Linting and Formatting
```bash
# Format code
yarn format

# Lint code
yarn lint
```

## 📝 API Endpoints

The API provides the following endpoints:

- `GET /articles` - Get all articles
- `GET /articles/:id` - Get article by ID
- `POST /articles` - Create a new article
- `PATCH /articles/:id` - Update an article
- `DELETE /articles/:id` - Delete an article

For detailed API documentation, visit the Swagger UI at `http://localhost:3000/api` when the application is running.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
