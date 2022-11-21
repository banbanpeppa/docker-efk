# EFK Docker

EFK - Elasticsearch Fluentd Kibana environment with one command line.

## Usage

```bash
docker-compose up -d
```

Tips: set fluentd address with `docker.for.mac.localhost:24224` on Mac M1/M2 otherwise `localhost:24224`
```
Mac M1/M2
fluentd-address: docker.for.mac.localhost:24224

Other
fluentd-address: localhost:24224
```

## Test

Generate httpd Access Logs by using curl command to generate some access logs like this:

```
while true; do curl http://localhost:8080/ ; sleep 2; done
```

Then, go to Discover tab to check the logs. As you can see, logs are properly collected into the Elasticsearch + Kibana, via Fluentd.

![img](https://1670780810-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LR7OsqPORtP86IQxs6E%2Fsync%2Fb83e35a5ba673b3c183d85a4406490f551fea50e.png?generation=1612863651409190&alt=media)