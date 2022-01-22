# Grafana Installation

## Deployment

Copy the `docker-compose.yml` template into your project folder and start the container.

## Configuration

Visit the Grafana Web Interface `http://localhost:3030`, and login with Grafana's default username and password: `admin`.

*For more info visit:* [Official Grafana Getting started Documentation](https://grafana.com/docs/grafana/latest/getting-started/getting-started/)

# Best-Practices & Post-Installation

## Disable HTTP

It's not secure to expose Grafana via the HTTP protocol. 

### Use a Reverse Proxy

- [ ] Use a Reverse Proxy to securely expose administrative services.

# Additional Referfences

[Official Grafana Documentation](https://grafana.com/docs/grafana/latest/)


# Prometheus Installation

## Deployment

1. Copy the configuration template into the `/etc/prometheus/prometheus.yml` location.
2. Copy the `docker-compose.yml` template into your project folder and start the container.

## Configuration

Configure your settings in the `/etc/prometheus/prometheus.yml` file.

*For more info visit:* [Official Prometheus Installation Documentation](https://prometheus.io/docs/prometheus/latest/installation/)

# Best-Practices & Post-Installation

## Disable HTTP

It's not secure to expose Prometheus via the HTTP protocol. 

### Use a Reverse Proxy

- [] Use a Reverse Proxy to securely expose administrative services.

# Additional Referfences

[Official Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)

# Cadvisor Exporter Dashboard ID - 14282
# Node Explorer Exporter Dashboard ID - 1860