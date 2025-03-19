## Full cluster restart upgrades

## Preparations for upgrade

- Shutdown logstash, beats and APM services
- [Create snapshots](https://www.elastic.co/guide/en/elasticsearch/reference/current/snapshots-take-snapshot.html)
- Export Kibana saved objects

### Upgrade Elasticsearch

[view upgrade guide](https://www.elastic.co/guide/en/elastic-stack/8.0/upgrading-elasticsearch.html)

#### Create symlinks

```sh
sudo -u elasticsearch ln -s /data/elasticsearch-7.9.1 /data/elasticsearch
```

#### Check and revise elasticsearch configuration

```sh
# check the configuration file
sudo cat /data/elasticsearch/config/elasticsearch.yml
```

Change jvm heap size in the jvm.options.d/heap_size.options file

```sh
# check the jvm options file
sudo cat /data/elasticsearch/config/jvm.options.d/heap_size.options

-Xms32g
-Xmx32g
```

#### Check and revise systemd service file

```sh
# check the service file
sudo cat /etc/systemd/system/elasticsearch.service

# reload the systemd service and restart the service
sudo systemctl daemon-reload
sudo systemctl restart elasticsearch
sudo systemctl status elasticsearch
```