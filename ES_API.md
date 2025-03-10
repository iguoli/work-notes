## ES API

## Cluster APIs

### Check cluster health
```sh
curl -X GET "localhost:9200/_cluster/health?pretty"
```

### List indices
```sh
curl -X GET "localhost:9200/_cat/indices?v"
```

### Create index
```sh
curl -X PUT "localhost:9200/test_index?pretty"
```

### Get index
```sh
curl -X GET "localhost:9200/test_index?pretty"
```

### Search index
```sh
curl -X GET "localhost:9200/test_index/_search?pretty"
```

### Insert document
```sh
curl -X PUT "localhost:9200/test_index/_doc/1" -H 'Content-Type: application/json' -d '{
    "name": "John Doe",
    "age": 30,
    "city": "New York"
}'
```

### Insert another document
```sh
curl -X PUT "localhost:9200/test_index/_doc/2" -H 'Content-Type: application/json' -d '{
    "name": "Jane Smith",
    "age": 25,
    "city": "Los Angeles"
}'
```

## ES Data Backup and Restore

### Create backup repository
```sh
curl -X PUT "localhost:9200/_snapshot/my_backup_repo" -H 'Content-Type: application/json' -d '{
    "type": "fs",
    "settings": {
        "location": "/home/guoli/es/backup-repo"
    }
}'
```

### Delete backup repository
```sh
curl -X DELETE "localhost:9200/_snapshot/my_backup_repo"
```

### List backup repositories
```sh
curl -X GET "localhost:9200/_snapshot?pretty"
```

### Create snapshot
```sh
curl -X PUT "localhost:9200/_snapshot/my_backup_repo/my_snapshot?wait_for_completion=true&pretty" -H 'Content-Type: application/json' -d '{
    "indices": "test_index",
    "ignore_unavailable": true,
    "include_global_state": false
}'
```

### Restore snapshot
```sh
curl -X POST "localhost:9200/_snapshot/my_backup_repo/my_snapshot/_restore?pretty"
```

### Restore snapshot
```sh
curl -X POST "localhost:9200/_snapshot/my_backup_repo/my_snapshot/_restore" -H 'Content-Type: application/json' -d '{
    "indices": "test_index",
    "ignore_unavailable": true,
    "include_global_state": false
}'
```

### List snapshots
```sh
curl -X GET "localhost:9200/_snapshot/my_backup_repo/_all?pretty"
```

### Delete snapshot
```sh
curl -X DELETE "localhost:9200/_snapshot/my_backup_repo/my_snapshot?pretty"
```
