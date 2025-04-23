## EMQX Operator

```sh
helm upgrade --install emqx-operator emqx/emqx-operator \
  --namespace emqx-operator-system \
  --create-namespace \
  --set "image.repository=cnnprcnn3abacusacr.azurecr.cn/emqx/emqx-operator-controller" \
  --set "image.tag=2.2.28" \
  --set "imagePullSecrets[0].name=emqx-registry"
```

```sh
helm upgrade --install abacus-emqx . --namespace emqx --create-namespace
```

```sh
kubectl create secret docker-registry emqx-registry \
  --docker-server=<registry> \
  --docker-username=<username> \
  --docker-password=<password> \
  --namespace=emqx-operator-system
```

## Prometheus

```sh
helm upgrade --install \
  --create-namespace \
  --namespace monitoring \
  my-prometheus \
  prometheus-community/prometheus \
  -f prometheus-values.yaml \
  -f alertmanager-values.yaml
```