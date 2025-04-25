# Accounting Software Docker Setup

This repository contains Docker configuration for running the Accounting Software application.

## Prerequisites

- Docker and Docker Compose installed on your system
- Git (to clone the repository)

## Getting Started

Follow these steps to run the application using Docker:

1. Clone the repository:
```
git clone <repository-url>
cd <repository-directory>
```

2. Start the application using Docker Compose:
```
docker-compose up -d
```

This command will:
- Build the Docker images for the frontend and backend
- Start the MySQL database container
- Initialize the database with the provided SQL file
- Start the backend API server
- Start the frontend React application

3. Access the application:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## Services

- **Database**: MySQL 5.7 running on port 3306
- **Backend**: Node.js API running on port 5000
- **Frontend**: React application running on port 3000

## Stopping the Application

To stop the application, run:
```
docker-compose down
```

To stop the application and remove all data volumes:
```
docker-compose down -v
```

## Troubleshooting

If you encounter any issues:

1. Check container logs:
```
docker-compose logs db
docker-compose logs backend
docker-compose logs frontend
```

2. Make sure all services are running:
```
docker-compose ps
```

3. To rebuild the containers after making changes:
```
docker-compose build
docker-compose up -d
``` # tien-hrm
