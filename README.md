# Confluent Platform (cp-all-in-one)
This repository provides Docker Compose files for quickly running the entire Confluent Platform, including Kafka broker, ZooKeeper, Schema Registry, Kafka Connect, Control Center, REST Proxy and ksqlDB.

**References:**
- https://github.com/confluentinc/cp-all-in-one
- https://docs.confluent.io/platform/current/platform-quickstart.html#:~:text=Quick%20Start%20for%20Confluent%20Platform%201%20Step%201%3A,stream%20and%20table%20by%20using%20SQL%20statements%20

# Quick Start
- **Remove interceptor class**  
    - Do not set Confluent interceptor classes—these are not in the community image.
    - For `ksqldb-server`, set these in `docker-compose.yml`:
    > ```yaml
    > KSQL_PRODUCER_INTERCEPTOR_CLASSES: ""
    > KSQL_CONSUMER_INTERCEPTOR_CLASSES: ""
    > ```
- Start all services with: 
    > ```sh
    > docker-compose up -d
    > ```

# Access to KsqlDB via Ksql-CLI
To open an interactive ksqlDB CLI session connected to your ksqlDB server, run:
```sh
docker exec -it ksqldb-cli ksql http://ksqldb-server:8088
docker exec -it ksqldb-cli ksql http://ksqldb-server:8088 -e "SHOW STREAMS;"
```


