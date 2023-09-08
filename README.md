# Spring Cloud Data Flow Development Environment

This Docker Compose setup provides a development environment for Spring Cloud Data Flow along with supporting services like MySQL, Kafka, Zookeeper, and Spring Cloud Skipper Server.

## Services

### MySQL (`dataflow-mysql`)

- **Purpose**: MySQL database service for Spring Cloud Data Flow.
- **Usage**: Provides the database backend for Spring Cloud Data Flow. It stores metadata, stream definitions, and task definitions.

### Spring Cloud Data Flow Server (`spring-data-flow-server`)

- **Purpose**: Core server for managing and orchestrating data pipelines.
- **Usage**: Offers a web-based dashboard for stream and task management.

### App Import Stream (`dataflow-app-import-stream`)

- **Purpose**: Service responsible for importing stream applications into Spring Cloud Data Flow.
- **Usage**: Automates the process of importing stream applications.

### App Import Task (`dataflow-app-import-task`)

- **Purpose**: Service responsible for importing task applications into Spring Cloud Data Flow.
- **Usage**: Automates the process of importing task applications.

### Spring Skipper Server (`spring-skipper-server`)

- **Purpose**: Provides server capabilities for deploying, managing, and updating Spring Cloud Data Flow applications.
- **Usage**: Facilitates the deployment and management of Data Flow applications.

### Kafka Broker (`dataflow-kafka`)

- **Purpose**: Kafka message broker used for building real-time data pipelines and streaming applications.
- **Usage**: Facilitates distributed event streaming for data pipelines.

### Zookeeper (`dataflow-kafka-zookeeper`)

- **Purpose**: Coordination service for distributed applications.
- **Usage**: Provides synchronization and configuration management for services in the ecosystem.

## Getting Started

1. **Installation**:
   - Ensure you have Docker and Docker Compose installed on your system.

2. **Starting the Environment**:
   - Run the following command in the directory containing `docker-compose.yml`:
     ```bash
     docker-compose up -d
     ```

3. **Accessing the Dashboard**:
   - Open your web browser and go to [http://localhost:9393](http://localhost:9393) to access the Spring Cloud Data Flow dashboard.

4. **Stopping the Environment**:
   - To stop the services, run:
     ```bash
     docker-compose down
     ```

## Important Notes

- **Security**: This setup is designed for development purposes. For production deployments, ensure secure settings, and protect sensitive information like passwords and access credentials.

- **Volumes**: This setup uses volumes to persist data. Ensure proper backup and recovery procedures for important data.

- **Customization**: You can customize the services and configurations in the `docker-compose.yml` file as per your requirements.

- **Dependencies**: Some services depend on others. Ensure that dependent services are up before starting a specific service.

## Additional Information

For more details about each service and how to customize configurations, refer to the [docker-compose.yml](docker-compose.yml) file.

For official documentation and resources, visit the [Spring Cloud Data Flow Documentation](https://dataflow.spring.io/docs/).
