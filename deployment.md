| commands                                                   | 
| :-------------------------                                 |
| kubectl create deployment --help |
| kubectl create -f deployment-definition.yaml               |             
| kubectl apply -f deployment-definition.yaml                |  
| kubectl create deployment [deployment-name] --image=[image-name] --replicas=3 | 
| kubectl create deployment [deployment-name] --image=[image-name] --replicas=3  --dry-run=client -o yaml > deployment-definition.yaml|
| kubectl get deployment                                     |             
| kubectl get deploy                                         |
| kubectl get all                                            |
| kubectl describe deployment                                |             
| kubectl describe deployment [deployment-name]              |             
| kubectl edit deployment [deployment-name]                  | 
| kubectl delete deployment [deployment-name]                |  


* Reference - https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
