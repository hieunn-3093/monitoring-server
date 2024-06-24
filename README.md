# monitoring-server

## Docker Compose Monitoring Stack

This repository contains a Docker Compose configuration to set up a monitoring stack using Prometheus, Grafana, and Node Exporter.

### Prerequisites

Before you begin, ensure you have the following installed:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

### Getting Started

1. **Clone the repository**

```bash
  git clone <repository_url>
  cd <repository_directory>
```

2. **Start the monitoring stack**

```bash
  docker-compose up -d --build
```

3. **Access Prometheus**

Prometheus is accessible at http://localhost:9090. You can use it to monitor and query your metrics.

4. **Access Grafana**

Grafana is accessible at http://localhost:6868. Use the following credentials to log in:

- Username: admin
- Password: admin

Grafana is preconfigured to connect to Prometheus as a data source.

4. **Explore and customize**
- Modify prometheus.yml to add more scrape configurations or adjust scrape intervals.
- Customize Grafana dashboards and explore metrics from Prometheus.

### Configuration Details
- Docker Compose Services:
  - node-exporter: Exposes host machine metrics.
  - prometheus: Monitoring and alerting toolkit.
  - grafana: Dashboard and graph editor for Graphite, InfluxDB, and OpenTSDB.
- Volumes:
  - grafana-data: Stores Grafana data persistently.
  - prometheus_data: Stores Prometheus data persistently.
- Network:
  - monitoring: Custom Docker network for internal communication between services.

### Additional Resources
- Prometheus Documentation
- Grafana Documentation
