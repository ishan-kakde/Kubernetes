
| commands                                                   | comment |
| :-------------------------                                 |:----------- |
| kubectl create -f replicaset-definition.yaml               |             |
| kubectl apply -f replicaset-definition.yaml                |             |
| kubectl get replicaset                                     |             |
| kubectl get rs                                             |             |
| kubectl describe rs [replicaset-name]                      |             |
| kubectl edit rs [replicaset-name]                          | reflects change immediately             |
| kubectl scale rs [replicaset-name] --replicas=5            | reflects change immediately             |
| kubectl delete replicaset [replicaset-name]                |             |


* Deployments are recommended over ReplicaSet.<br>
* Reference - https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/
