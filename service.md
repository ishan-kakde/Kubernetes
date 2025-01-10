|commands|
|:------------|
|kubectl create -f [service-definition.yaml]|
|kubectl create service nodeport nginx --tcp=80:80 --node-port=30080 --dry-run=client -o yaml|
|kubectl create service clusterip redis --tcp=6379:6379 --dry-run=client -o yaml|
|kubectl expose pod nginx --port=80 --name=nginx-service --type=NodePort --dry-run=client -o yaml _(creates and maps service to pod)_|
|kubectl run httpd --image=httpd:alpine --port=80 --expose _(this command creates both service and pod)_|
|minikube |
|minikube service [service-name] --url _(to access container when using minikube cluster)_|
|localhost:node-port _(to access container when using docker kubernetes cluster)_|
|https://minikube.sigs.k8s.io/docs/handbook/accessing/#using-minikube-service-with-tunnel|
|https://stackoverflow.com/questions/57021939/docker-for-desktop-runs-the-kubernetes-ip-address-is-not-working|

#32
