## Full cluster restart upgrades

### Checking list before upgrading

- Kibana saved objects checking

- Check all data sources have been shutdown before upgrading to new version

1. Disable shard allocation

```sh
curl -X PUT "localhost:9200/_cluster/settings?pretty" -H 'Content-Type: application/json' -d'
{
    "persistent": {
        "cluster.routing.allocation.enable": "none"
    }
}
'
```

2. Stop all Elasticsearch nodes and upgrade them
3. Upgrade any plugins
4. Start the Elasticsearch cluster

    Keep in mind that during a full cluster restart, **the master nodes need to be initiated prior to the non-master nodes.** This is essential for allowing the master nodes to establish the cluster so that other nodes can join

5. Re-enable shard allocation

```sh
curl -X PUT "localhost:9200/_cluster/settings?pretty" -H 'Content-Type: application/json' -d'
{
    "persistent": {
        "cluster.routing.allocation.enable": null
    }
}
'
```

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