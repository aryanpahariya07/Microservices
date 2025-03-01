# Microservices Project

## Overview
This project is a **microservices-based architecture** developed using **Java Spring Boot**. It consists of multiple independent services that communicate via REST APIs. The key services in this project include:

- **BillingService**: Handles invoice generation and payment processing.
- **SubscriptionService**: Manages user subscriptions, account creation, and renewals.
- **SupportService**: Provides customer support by handling tickets and queries.

Each service follows a modular design, allowing for independent development, deployment, and scaling.

## Technologies Used

### Backend Technologies
- **Java 17**: Primary programming language.
- **Spring Boot**: Framework for building RESTful microservices.
- **Spring Data JPA**: Simplifies database interaction using ORM.
- **Spring Cloud OpenFeign**: Enables service-to-service communication.
- **Spring Security**: Ensures authentication and authorization.
- **Hibernate**: ORM framework for handling database operations.
- **Lombok**: Reduces boilerplate code with annotations.

### Database
- **PostgreSQL/MySQL**: Relational database for storing application data.
- **Flyway**: Manages database versioning and migrations.

### API Communication
- **RESTful APIs**: Exposes endpoints for service interaction.
- **Swagger/OpenAPI**: API documentation and testing.

### Containerization & Deployment
- **Docker**: Containerizes each microservice for easy deployment.
- **Docker Compose**: Orchestrates multiple microservices.
- **Kubernetes (Optional)**: Manages containerized services at scale.

### Monitoring & Logging
- **Spring Boot Actuator**: Provides operational insights.
- **Prometheus & Grafana (Optional)**: Monitors system performance.
- **ELK Stack (Elasticsearch, Logstash, Kibana)**: Aggregates and visualizes logs.

## Setup Instructions

1. Clone the repository:
   ```sh
   git clone <repository_url>
   cd Microservices
   ```

2. Navigate to each service directory and build the project:
   ```sh
   cd BillingService
   mvn clean install
   cd ../SubscriptionService
   mvn clean install
   cd ../SupportService
   mvn clean install
   ```

3. Configure database settings in `application.properties` or `application.yml`.

4. Run each service:
   ```sh
   mvn spring-boot:run
   ```
   or, if using Docker:
   ```sh
   docker-compose up
   ```

## API Endpoints
Each service provides RESTful APIs for external interaction:

### Billing Service
- `POST /invoice` - Create an invoice
- `POST /payment` - Process a payment

### Subscription Service
- `POST /user` - Register a new user
- `POST /subscription` - Create a subscription

### Support Service
- `POST /ticket` - Raise a support ticket
- `GET /ticket/{id}` - Get ticket details




