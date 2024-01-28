# Logging with Vector, Loki and Grafana

This is an example setup on how to collect Docker logs in Loki using Vector. They can then be explored using Grafana.

## Components

### Vector

[Vector](https://vector.dev) is used to collect the logs and write them to Loki in this example. In more complex cases, it can also transform or enrichs them. It also writes its own logs into Loki.

### Loki

[Loki](https://grafana.com/oss/loki/) is used as a storage and query engine for the logs. In this configuration it uses the local filesystem to store the data without replication. Statistics reporting back to Grafana Labs is disabled.

### Grafana

[Grafana](https://grafana.com/grafana/) can be used to explore the logs and to create dashboards. Loki as a datasource is provisioned at startup and logs should directly appear in the Explore view. Initial credentials are `admin:admin`. The frontend can be reached under `localhost:3000`.

https://betterstack.com/community/guides/logging/vector-explained/
https://betterstack.com/community/guides/logging/how-to-start-logging-with-docker/
https://betterstack.com/community/guides/logging/how-to-start-logging-with-laravel/
