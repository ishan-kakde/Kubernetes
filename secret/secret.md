|commands|
|:-------|
|kubectl create -f secret-definition.yaml _(using declarative approach - data/secret values must be provided in encoded form)_|
|kubectl create secret generic  [secret-name] --from-file=secret-data.properties |
|kubectl create secret generic  [secret-name] --from-literal=key1=value1 --from-literal=key2=value2 |
|kubectl create secret generic  [secret-name] --from-literal=key1=value1 --from-literal=key2=value2 --dry-run=client -o yaml |
|kubectl get secrets _(does not show the value of the secret)_|
|kubectl get secrets [secret-name] -o yaml _(shows the value of the secret)_|
|kubectl describe secrets [secret-name]|
|kubectl delete secrets [secret-name] |


Reference - <br>
https://kubernetes.io/docs/concepts/configuration/secret/<br>
https://kubernetes.io/docs/tasks/configmap-secret/<br>

