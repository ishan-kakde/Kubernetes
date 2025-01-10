|commands|
|:------------|
|kubectl create -f [service-definition.yaml]|
|kubectl create service nodeport nginx --tcp=80:80 --node-port=30080 --dry-run=client -o yaml|
|kubectl create service clusterip redis --tcp=6379:6379 --dry-run=client -o yaml|
|kubectl expose pod nginx --port=80 --name nginx-service --type=NodePort --dry-run=client -o yaml|
|kubectl run httpd --image=httpd:alpine --port=80 --expose _(this command creates both service and pod)_|
|minikube |
|minikube service [service-name] --url |

#32
