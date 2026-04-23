
# Shipping-Management-System_Java-Backend
Building a Scalable Microservices Application with Java Spring Boot and Angular

<img width="1024" height="559" alt="005ab02b-be51-4fbe-8cae-879a5be1ba54" src="https://github.com/user-attachments/assets/6126a258-3647-450a-84a9-1d3f07a0b054" />


- Frontend Access: User uses the Angular app.
- API Gateway: All frontend requests pass through the Spring Cloud Gateway, which handles routing and validates JWTs (provided by the IAM Service).
- Sync Communication (REST): The frontend makes immediate calls to IAM, Order, and Fleet services (e.g., to view order history).
- Async Events (Kafka): This is the core engine.
- Order Service -> order-created topic.
- Fleet Service (Consumes order-created) -> Assigns penguin -> publishes to penguin-assigned topic.
- Worker Penguins (External Input) -> Publish high-throughput location-update events to Kafka.
- Real-Time Push (WebSockets): The Tracking Service consumes location-update events from Kafka and opens a persistent WebSocket connection with the Angular frontend to push live tracking and notifications directly to Dennis.
- Infrastructure: All components are containerized (Docker) and managed within a Kubernetes Cluster for scaling and orchestration.
- Start by defining the API Contracts and DB Schema for the first microservice (e.g., Identity/IAM or Order Management).
- Set up the initial Docker Compose environment for local development (PostgreSQL, Kafka, Zookeeper).
