# Base Services with Docker Compose

This repository provides a Docker Compose configuration for commonly used base services such as PostgreSQL, Redis, RabbitMQ, etc. These services are essential for many applications and serve as foundational building blocks for modern development.

## Services Included

1. **PostgreSQL**
   - Database service for relational data.
   - Exposed on port `5432`.

2. **Redis**
   - In-memory data structure store, used as a database, cache, and message broker.
   - Exposed on port `6379`.

3. **RabbitMQ**
   - Message broker for asynchronous communication.
   - Ports:
     - `5672`: For messaging.
     - `15672`: Management UI.

4. **Elasticsearch**
   - Distributed search and analytics engine.
   - Exposed on port `9200`.

5. **Grafana**
   - Visualization and monitoring platform.
   - Exposed on port `3000`.

6. **MySQL**
   - Database service for relational data.
   - Exposed on port `3306`.

7. **Portainer**
   - Lightweight management UI for Docker.
   - Exposed on port `9000`.

## Prerequisites

- Install [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/).
- Ensure enough system resources are available (RAM, CPU, and storage).

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/muharamdani/base-services.git
   cd base-services
   ```

2. Start the services:
   ```bash
   docker-compose up -d
   ```

3. Verify services are running:
   - PostgreSQL: Connect on `localhost:5432`.
   - MySQL: Connect on `localhost:3306`.
   - Redis: Connect on `localhost:6379`.
   - RabbitMQ Management UI: [http://localhost:15672](http://localhost:15672).
   - Elasticsearch: [http://localhost:9200](http://localhost:9200).
   - Grafana: [http://localhost:3000](http://localhost:3000).
   - Portainer: [http://localhost:9000](http://localhost:9000).

4. Stop the services:
   ```bash
   docker-compose down
   ```

## Customization

- Update credentials or configurations in the `docker-compose.yml` file as needed.
- Add or remove services based on your stack requirements.

## Troubleshooting

- Check service logs using:
  ```bash
  docker-compose logs <service_name>
  ```
  Replace `<service_name>` with `postgres`, `redis`, `rabbitmq`, etc.

- Ensure ports are not already in use on your system.

## License

This project is open-source and licensed under the [MIT License](LICENSE).
