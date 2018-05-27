# prometheus-sample

Work prometheus and collect sample data from dependened docker containers.
And rednering chart with grafana

## Getting Started

```
git clone <this>
git submdule init --update

docker-compose up grafana
```

## Dashboards

name | url
--- | ---
Grafana dashboard  | http://localhost:3000
prometheus dashboard  | http://localhost:9090/graph

## Sample Prometheus Queries

For prometheus

```
prometheus_target_interval_length_seconds
```

For random

```
avg(rate(rpc_durations_seconds_count[5m])) by (job, service)
avg(rate(rpc_durations_seconds_count[5m])) by (group)
```

## Other Usage

command via console container

```
docker-compose exec console sh

# examples
$ curl prometheus:9090/graph
$ curl random-8080:8080/metrics
```


