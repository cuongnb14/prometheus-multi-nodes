# Monitoring multi Hosts and Docker Containers

## Information

- Prometheus v2.10.1
- Node Exporter v1.0.1
- Cadvisor v0.36.0
- Grafana v7.1.5

Dashboards:

- https://grafana.com/grafana/dashboards/8321
- https://grafana.com/grafana/dashboards/11074

## Setup:

### Center Node
```
git clone https://github.com/cuongnb14/prometheus-multi-nodes.git prometheus

docker-compose up -d
```

### Agent Node
```
wget https://raw.githubusercontent.com/cuongnb14/prometheus-multi-nodes/master/docker-compose.exporter.yml -O docker-compose.yml

# Note: update hostname for containers to display in dashboard
docker-compose up -d
```

Re-config `prometheus/prometheus.yml` in Center node