
| commands    |                                              
| :-------------------------                                 
| kubectl create -f pod-definition.yaml|
| kubectl apply -f pod-definition.yaml|
| kubectl run nginx --image=nginx |             
| kubectl run nginx --image=nginx -n=dev_namespace |             
| kubectl run redis --image=redis --dry-run=client -o yaml |             
| kubectl run redis --image=redis --dry-run=client -o yaml > pod-definition.yaml|
| kubectl run redis -l tier=db --image=redis:alpine |
| kubectl run custom-nginx --image=nginx --port=8080 |
| kubectl get pod [pod-name] -o yaml > pod-definition.yaml|
| kubectl get pods |
| kubectl get po |
| kubectl get po -A|
| kubectl get po -o wide|
| kubectl describe pod [pod-name]  |            
| kubectl edit pod [pod-name] _(creates a temp pod definition file, delete existing pods then create new pods using temp file)_|
| kubectl exec [ubuntu-pod] -- whoami |
| kubectl replace --force -f updated-pod-definition.yaml|
| kubectl delete pod [pod-name]|


