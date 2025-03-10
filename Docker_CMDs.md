Run a filebeat container and connect to a specified elasticsearch service

```sh
docker run -d \
  --name=filebeat \
  --user=root \
  --volume="$(pwd)/filebeat.docker.yml:/usr/share/filebeat/filebeat.yml:ro" \
  --volume="/var/lib/docker/containers:/var/lib/docker/containers:ro" \
  --volume="/var/run/docker.sock:/var/run/docker.sock:ro" \
  -e --strict.perms=false \
  -e output.elasticsearch.hosts="localhost:9200" \
  elastic/filebeat:8.17.2 filebeat
```

Run a Kibana instance and connect to a specified elasticsearch service

```sh
docker run --rm -d --name kibana-7.17 --net bridge -p 5601:5601 -e ELASTICSEARCH_HOSTS="http://10.94.144.71:19200" kibana:7.17.17
```
