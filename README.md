# Microservices Project

## Overview

This project is a microservices-based application implemented using **Java Spring Boot**. It consists of the following services:

- **BillingService**: Manages invoices and payments.
- **SubscriptionService**: Handles user accounts, subscriptions, and related operations.
- **SupportService**: Manages support tickets and troubleshooting logs.

Each microservice is structured with controllers, services, models, and repositories following the MVC pattern.

## Prerequisites

Before running the project, ensure you have the following installed:

- **Java 17 or later**
- **Maven** (for dependency management and build)
- **Docker** (if containerization is required)
- **PostgreSQL/MySQL** (depending on the database configuration)

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

3. Configure database settings in `application.properties` or `application.yml` in each service.

4. Run each service:

   ```sh
   mvn spring-boot:run
   ```

   or, if using Docker:

   ```sh
   docker-compose up
   ```

## API Endpoints

Each service exposes REST endpoints for interaction:

### Billing Service

- `POST /invoice` - Create an invoice
- `POST /payment` - Process a payment

### Subscription Service

- `POST /user` - Register a new user
- `POST /subscription` - Create a subscription

### Support Service

- `POST /ticket` - Raise a support ticket
- `GET /ticket/{id}` - Get ticket details

## Technologies Used

- **Spring Boot** (REST APIs, MVC architecture)
- **Spring Data JPA** (Database interaction)
- **Spring Cloud OpenFeign** (Inter-service communication)
- **Docker** (Containerization)
- **PostgreSQL/MySQL** (Database)

## Contribution

Feel free to fork the repository, create a branch, and submit a pull request for improvements.

## License

This project is licensed under [MIT License](LICENSE).

