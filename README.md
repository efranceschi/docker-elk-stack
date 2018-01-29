# docker-elk-stack

docker-elk-stack is an [ELK](https://www.elastic.co/webinars/introduction-elk-stack) Stack Template to deploy into [Docker Swarm](https://docs.docker.com/engine/swarm/) environment.

## Quick start

1. Clone this repository
```
git clone https://github.com/efranceschi/docker-elk-stack.git
```

2. Enter directory
```
cd docker-elk-stack
```

3. Create config
```
docker config create elasticsearch_config example-elasticsearch.yml
docker config create logstash_config example-logstash-config.yml
docker config create logstash_pipeline example-logstash-pipeline.conf
docker config create kibana_config example-kibana.yml
```

4. Start the stack
```
docker stack deploy -c docker-compose.yml elk
```

## Uninstalling

```
docker stack rm elk
docker config rm elasticsearch_config
docker config rm logstash_config
docker config rm logstash_pipeline
docker config rm kibana_config
```
