| commands                                                   | 
| :-------------------------                                 |
| kubectl create deployment --help |
| kubectl create -f deployment-definition.yaml               |
| kubectl create -f deployment-definition.yaml --record _(records the cause of the change)_            |
| kubectl apply -f deployment-definition.yaml                |  
| kubectl create deployment [deployment-name] --image=[image-name] --replicas=3 | 
| kubectl create deployment [deployment-name] --image=[image-name] --replicas=3  --dry-run=client -o yaml > deployment-definition.yaml|
| kubectl get deployment                                     |             
| kubectl get deploy                                         |
| kubectl get all                                            |
| kubectl describe deployment                                |             
| kubectl describe deployment [deployment-name]              |             
| kubectl edit deployment [deployment-name]  _(deployment automatically deletes old and creates new pods)_ | 
| kubectl delete deployment [deployment-name]                |  
| kubectl set image deployment [deployment=name] nginx=nginx:1.18-perl --record |


* Reference - https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
