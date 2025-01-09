
| commands                                                   | 
| :-------------------------                                 |
| kubectl create -f replicaset-definition.yaml               |             
| kubectl apply -f replicaset-definition.yaml                |
| kubectl replace -f replicaset-definition-updated.yaml      |
| kubectl scale --replicas=5 -f replicaset-definition.yaml _(this command does not update the file)_  |
| kubectl get replicaset                                     |             
| kubectl get rs                                             |            
| kubectl describe rs [replicaset-name]                      |             
| kubectl edit rs [replicaset-name]                          | 
| kubectl scale rs [replicaset-name] --replicas=5            | 
| kubectl delete replicaset [replicaset-name]   _(deletes underlying pods as well)_             |             


* Deployments are recommended over ReplicaSet.<br>
* Reference - https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/
