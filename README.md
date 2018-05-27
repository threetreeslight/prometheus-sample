# prometheus-sample


## Getting Started

clone

```
git clone this
git submdule init --update
```

run

```
docker-compose up prometheus
```

You can see prometheus on `localhost:9090`

And some command via console

```
docker-compose exec console sh

# examples
$ curl prometheus:9090/graph
$ curl random-8080:8080/metrics
```

# Sample Prometheus Queries

For prometheus


For random

```
avg(rate(rpc_durations_seconds_count[5m])) by (job, service)
avg(rate(rpc_durations_seconds_count[5m])) by (group)
```
