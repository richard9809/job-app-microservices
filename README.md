# Job Application Microservices Platform

A modern, distributed job application platform built using microservices architecture. This system allows companies to post jobs and manage applications while providing job seekers with a seamless application experience.

## 🚀 Overview

This platform is built using a microservices architecture, which means it's composed of several independent services that work together to provide a complete job application system. Each service is containerized using Docker for easy deployment and scalability.

## 🏗 System Architecture

The system consists of the following main components:

1. **Config Server** - Centralizes configuration management for all services
2. **Service Registry** - Handles service discovery and registration
3. **Company Service** - Manages company profiles and job postings
4. **Job Service** - Handles job-related operations
5. **Review Service** - Manages company reviews and ratings

## 🔧 Technical Stack

- **Backend**: Spring Boot Microservices
- **Database**: PostgreSQL
- **Service Discovery**: Eureka Server
- **Configuration**: Spring Cloud Config
- **Containerization**: Docker
- **API Gateway**: Spring Cloud Gateway
- **Database Admin**: PgAdmin4

## 🚦 Prerequisites

To run this application, you'll need:

- Docker and Docker Compose
- Java 17 or higher
- Maven
- PostgreSQL (if running locally)

## 🏃‍♂️ Getting Started

### Running with Docker (Recommended)

1. Clone the repository
2. Navigate to the project root directory
3. Run the following command:
```bash
docker-compose up
```

This will start all the necessary services including:
- PostgreSQL database (port 5432)
- PgAdmin4 (port 5050)
- Config Server (port 8080)
- Service Registry (port 8761)
- And all other microservices

### Accessing Services

- **PgAdmin**: http://localhost:5050
  - Default email: pgadmin4@pgadmin.org
  - Default password: admin
- **Service Registry Dashboard**: http://localhost:8761
- **API Gateway**: http://localhost:8080

## 🔐 Security

The application uses Spring Security for authentication and authorization. Make sure to set up proper environment variables for sensitive information like database credentials and API keys.

## 🛠 Development

Each microservice is a separate Spring Boot application that can be developed and deployed independently. The services communicate with each other through REST APIs and are registered with the Eureka service registry.

### Project Structure
```
job-app-microservices/
├── ConfigServer/         # Configuration management
├── companyms/           # Company management service
├── jobms/              # Job posting service
├── reviewms/           # Review management service
└── docker-compose.yaml  # Docker composition file
```

## 📝 Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
