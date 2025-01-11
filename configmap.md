|commands|
|:-------|
|kubectl create configmap  [configmap-name] --from-file=configmap-definition.yaml |
|kubectl create configmap  [configmap-name] --from-env-file=configmap-definition.yaml |
|kubectl create configmap  [configmap-name] --from-literal=key1=value1 --from-literal=key2=value2 |
|kubectl create configmap  [configmap-name] --from-literal=key1=value1 --from-literal=key2=value2 --dry-run=client -o yaml |
|kubectl get configmap |
|kubectl create describe configmap [configmap-name]|
|kubectl create delete configmap [configmap-name] |
