# Shipping-Management-System_Java-Backend
Building a Scalable Microservices Application with Java Spring Boot and Angular

<img width="742" height="805" alt="image" src="https://github.com/user-attachments/assets/1f65d1c8-05ae-4f9f-80f5-ec126c540529" />




Architecture Highlights:

- 6 Core Microservices: Order, Delivery, Tracking, Notification, User/Penguin, and Analytics services
- Event-Driven: Apache Kafka for asynchronous communication between services
- Real-time Updates: WebSocket integration for live notifications and location tracking
- Scalable Infrastructure: Kubernetes orchestration with Docker containers
- Security: JWT/OAuth 2.0 authentication with RBAC
- Data Management: PostgreSQL for relational data, Redis for caching, S3 for files

Key Components:

- Angular frontend with NgRx for state management
- API Gateway for request routing and authentication
- Microservices layer with clear separation of concerns
- PostgreSQL + Redis + Kafka for data and event management
- WebSocket servers for real-time communication
- Comprehensive monitoring with ELK stack

Design Principles:

- Service independence and scalability
- Event-driven asynchronous workflows
- Real-time first approach with WebSockets
- Comprehensive logging, monitoring, and testing
- Docker containerization and Kubernetes orchestration
