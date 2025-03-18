## Full cluster restart upgrades

## Create snapshots

[Restore a snapshot](https://www.elastic.co/guide/en/elasticsearch/reference/current/snapshots-restore-snapshot.html)

## Create symlinks

```sh
sudo chown elasticsearch:elasticsearch /data/
sudo -u elasticsearch ln -s /data/elasticsearch-7.9.1 /data/elasticsearch
```

## Check and revise elasticsearch configuration

```sh
# check the configuration file
sudo cat /data/elasticsearch/config/elasticsearch.yml
```

## Check and revise systemd service file

```sh
# check the service file
sudo cat /etc/systemd/system/elasticsearch.service

# reload the systemd service and restart the service
sudo systemctl daemon-reload
sudo systemctl restart elasticsearch
sudo systemctl status elasticsearch
```

### Checking list before upgrading

- Kibana saved objects checking

- Check all data sources have been shutdown before upgrading to new version

1. Disable shard allocation
2. Stop all Elasticsearch nodes and upgrade them
3. Upgrade any plugins
4. Start the Elasticsearch cluster
    Keep in mind that during a full cluster restart, **the master nodes need to be initiated prior to the non-master nodes.** This is essential for allowing the master nodes to establish the cluster so that other nodes can join
5. Re-enable shard allocation
6. Upgrade client libraries to new version
7. Restart master eligible nodes
8. Restart non-master eligible nodes

## Elasticsearch 8 Breaking Changes

### Elasticsearch 8 configuration file

Breaking changes in `elasticsearch.yml`

```yaml
# transport.tcp.port replaced by transport.port
transport.port: 9300

# discovery.zen settings have been removed.

# Encrypting communications between nodes in a cluster. 
xpack.security.transport.ssl.enabled: false

# Encrypting HTTP client communications
xpack.security.http.ssl.enabled: false
```

### Kibana configuration file

Breaking changes in `kibana.yml`

```yaml
elasticsearch.username: kibana_system
```