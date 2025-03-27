helm upgrade --install emqx-operator emqx/emqx-operator \
  --namespace emqx-operator-system \
  --create-namespace \
  --set "image.repository=cnnprcnn3abacusacr.azurecr.cn/emqx/emqx-operator-controller" \
  --set "image.tag=2.2.28" \
  --set "imagePullSecrets[0].name=emqx-registry"

kubectl create secret docker-registry emqx-registry \
  --docker-server=<registry> \
  --docker-username=<username> \
  --docker-password=<password> \
  --namespace=emqx-operator-system
