# Confluent Platform (cp-all-in-one)
This repository provides Docker Compose files for quickly running the entire Confluent Platform, including Kafka broker, ZooKeeper, Schema Registry, Kafka Connect, Control Center, REST Proxy and ksqlDB.

**References:**
- https://github.com/confluentinc/cp-all-in-one
- https://docs.confluent.io/platform/current/platform-quickstart.html#:~:text=Quick%20Start%20for%20Confluent%20Platform%201%20Step%201%3A,stream%20and%20table%20by%20using%20SQL%20statements%20

# Services and Ports
- Access **Confluent Control Center** at [http://localhost:9021](http://localhost:9021)

| Service                | Port   |
|------------------------|--------|
| Kafka broker           | 9092   |
| ZooKeeper              | 2181   |
| Schema Registry        | 8081   |
| Kafka Connect          | 8083   |
| Control Center         | 9021   |
| ksqlDB                 | 8088   |
| REST Proxy             | 8082   |
| Flink Job Manager      | 9081   |

