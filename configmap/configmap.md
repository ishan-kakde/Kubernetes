|commands|
|:-------|
|kubectl create configmap  [map-name] --from-file=configmap-definition.yaml |
|kubectl create configmap  [map-name] --from-env-file=configmap-definition.properties |
|kubectl create configmap  [map-name] --from-literal=key1=value1 --from-literal=key2=value2 |
|kubectl create configmap  [map-name] --from-literal=key1=value1 --from-literal=key2=value2 --dry-run=client -o yaml |
|kubectl get configmap|
|kubectl get configmap [map-name] -o yaml|
|kubectl describe configmap [map-name]|
|kubectl delete configmap [map-name] |
 
