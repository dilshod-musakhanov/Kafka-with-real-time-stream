## Wikimedia Updates Kafka Integration

#### This project demonstrates the integration of Kafka with a web service to stream real-time updates from the Wikimedia website. The updates are then processed by a Kafka producer and consumed by a Kafka consumer, which saves the data into a database.

---

#### The project consists of the following components:

- **Producer:** The producer component establishes a connection to the Wikimedia updates stream endpoint (https://stream.wikimedia.org/v2/stream/recentchange) using the EventSource library. It listens for updates from the web service and publishes them to a Kafka topic.

- **Consumer:** The consumer component subscribes to the Kafka topic where the updates are published. It listens for incoming messages and processes them, in this case, saving them to a database.

#### Technologies Used
```
Spring Boot
Spring Kafka
EventSource
Apache Kafka
Hibernate
PostgreSql
Liquibase
```

#### To run the project:
- Make sure you have Apache Kafka installed and running locally.
- Configure the Kafka broker and database connection settings in the application.properties file.
- Start Zookeeper server then Kafka server.
- Start the Kafka producer and consumer modules.
- The producer will start streaming updates from the Wikimedia website and publishing them to a Kafka topic.


.
The consumer will subscribe to the Kafka topic, consume the messages, and save them to the database.
