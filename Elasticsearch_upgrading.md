## Elastic Search 8 Breaking Changes

### Elastic search configuration file

Breaking changes in `elasticsearch.yml`

```yaml
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