
|**About Pods**|
|:------|
|**Pods** are the smallest deployable units of computing that you can create and manage in Kubernetes|
|**Pods with single container** - The "one-container-per-Pod" model is the most common Kubernetes use case; in this case, you can think of a Pod as a wrapper around a single container; Kubernetes manages Pods rather than managing the containers directly|
|**Pods with multiple containers** A Pod can have multiple co-located and co-scheduled containers that are tightly coupled and need to share resources. These co-located containers form a single cohesive unit. Grouping multiple co-located and co-managed containers in a single Pod is a relatively advanced use case, you should use this pattern only if your containers are tightly coupled|
|**Sidecar** containers are the secondary containers that run along with the main application container within the same Pod. These containers are used to enhance or to extend the functionality of the primary app container by providing additional services, or functionality such as logging, monitoring, security, or data synchronization, without directly altering the primary application code.|
|**Sidecar** container starts before the main application container and continues to run along main container|
|**Init containers** run and complete their tasks before the main application container starts. Unlike sidecar containers, init containers are not continuously running alongside the main containers|
|A Pod may have one or more multiple init containers. **Init containers** run to completion sequentially, and the main container does not start until all the init containers have successfully completed.|
|**Pod Lifecycle** - Pods follow a defined lifecycle, starting in **Pending**, then to **Running** if atleast one primary container starts OK, then to **Succeeded or Failed** depending upon whether container in pod terminated in failure|
|When a pod is failing to start repeatedly, **CrashLoopBackOff** may appear in the **Status** field of some kubectl commands. Similarly, when a pod is being deleted, **Terminating** may appear in the **Status** field of some kubectl commands|
|Kubernetes tracks the state of each container inside a Pod. There are three possible container states: **Waiting, Running, and Terminated**.|
|Assigning a Pod to a specific node is called **binding** and process to select which node to use is called **scheduling** |

<br><br>

|**commands**|
|:------|                                                                       
| kubectl create -f pod-definition.yaml|
| kubectl apply  -f pod-definition.yaml|
| kubectl run [pod-name] --image=[image-name] |             
| kubectl run [pod-name] --image=[image-name] -n=[namespce] |             
| kubectl run [pod-name] --image=[image-name] --dry-run=client -o yaml |             
| kubectl run [pod-name] --image=[image-name] --dry-run=client -o yaml > pod-definition.yaml|
| kubectl run [pod-name] --image=[image-name] --port=8080 |
| kubectl run [pod-name] -l [label-name]=[label-value] --image=[image-name] |
| kubectl get pod [pod-name] -o yaml > pod-definition.yaml|
| kubectl get pods |
| kubectl get po |
| kubectl get po -A|
| kubectl get po -o wide|
| kubectl describe pod [pod-name]  |            
| kubectl edit pod [pod-name] _(creates a temp pod definition file, delete existing pods then create new pods using temp file or use replace command)_|
| kubectl exec [ubuntu-pod] -- whoami |
| kubectl replace --force -f updated-pod-definition.yaml _(force deletes existing pods and recreates them with latest changes)_|
| kubectl delete pod [pod-name]|

<br><br>

**Reference** - <br>
https://kubernetes.io/docs/concepts/workloads/pods<br>
https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/<br>
https://kubernetes.io/docs/concepts/workloads/pods/sidecar-containers<br>
https://kubernetes.io/docs/concepts/workloads/pods/init-containers<br>
