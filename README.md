# E-Commerce Microservices App

## Overview
This is a **scalable E-Commerce microservices platform** built using:
- **Backend**: Spring Boot, Kafka, Spring Cloud, MySQL, Redis, JWT, Docker
- **Frontend**: React.js, Redux, Tailwind CSS
- **Messaging**: Apache Kafka
- **Service Discovery & API Gateway**: Spring Cloud Gateway & Eureka
- **Deployment**: Docker, Kubernetes

## Features
- User authentication (JWT-based)
- Product catalog service
- Order service with Kafka-based event-driven processing
- Inventory management
- Payment processing simulation
- Frontend with React.js and Redux

## Project Structure
```
E-Commerce-Microservices-App/
│── backend/
│   ├── api-gateway/
│   ├── auth-service/
│   ├── product-service/
│   ├── order-service/
│   ├── inventory-service/
│   ├── payment-service/
│   ├── common-config/
│── frontend/
│   ├── src/
│   ├── public/
│── kafka/
│── docker/
│── k8s/
│── README.md
```

### Backend Microservices
- `api-gateway`: Handles routing and authentication
- `auth-service`: Manages user authentication
- `product-service`: Handles product catalog
- `order-service`: Processes orders and publishes events to Kafka
- `inventory-service`: Updates stock based on order events
- `payment-service`: Simulates payment processing
- `common-config`: Shared configurations

### Frontend
- Built with **React.js** & **Redux**
- Styled with **Tailwind CSS**
- API calls using **Axios**

### Kafka Topics
- `order-events`
- `payment-events`

### Running the Project
1. Start Kafka & Zookeeper:
   ```bash
   docker-compose up -d
   ```
2. Run backend services:
   ```bash
   mvn spring-boot:run
   ```
3. Start frontend:
   ```bash
   cd frontend && npm start
   ```

## Deployment
- **Docker Compose** for local setup
- **Kubernetes (K8s)** for production deployment

## Contributing
1. Fork the repo
2. Create a feature branch
3. Submit a PR

## License
MIT License

