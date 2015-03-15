# Multiple dependencies

This demo shows how to start in Docker multiple dependencies that are required by your application on a local machine using Docker Compose.

This demo starts RabbitMQ broker, ElasticSearch using their based image and Neo4J using a custom Dockerfile.

First, you need to install [Docker and Docker Compose](https://docs.docker.com/compose/#installation-and-set-up).

## Run the demo
To run the demo, you just need to start Docker Compose:
```
docker-compose up
```
This command creates tree docker containers one for each system (RabbitMQ, ElasticSearch and Neo4J).

You can access each system using the following URL:
- RabbitMQ: http://localhost:15672
- Neo4j : http://localhost:7474
- ElasticSearch : http://localhost:9200

You can check the containers status using the command:
```
docker-compose ps
```

The data and logs are located inside the compose directory.

