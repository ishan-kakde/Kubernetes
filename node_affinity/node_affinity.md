|**commands**||
|:-------|:--------|
|get label|kubectl get nodes --show-labels|
|create label|kubectl label nodes [node-name] [lable-key]=[label-value]|
|pod with node info|kubectl get pods -o wide|



|**summary**|
|:------|
|nodeSelector is the simplest way to constraint pods to node with specific label|
|Node affinity functions like the nodeSelector field but is more expressive and allows you to specify preferred or required rules|
|The affinity and anti-affinity language is more expressive. nodeSelector only selects nodes with all the specified labels. Affinity and anti-affinity gives you more control over the selection logic|
|You can indicate that a rule is soft or preferred, so that the scheduler still schedules the Pod even if it can't find a matching node|
|There are two types of node affinity - <br> requiredDuringSchedulingIgnoredDuringExecution<br>requiredDuringSchedulingIgnoredDuringExecution|
|**requiredDuringSchedulingIgnoredDuringExecution** - The scheduler can't schedule the Pod unless the rule is met. This functions like nodeSelector, but with a more expressive syntax|
|**preferredDuringSchedulingIgnoredDuringExecution** - The scheduler tries to find a node that meets the rule. If a matching node is not available, the scheduler still schedules the Pod.|
|**IgnoredDuringExecution** means that if the node labels change after Kubernetes schedules the Pod, the Pod continues to run|
|logical **operators** are **In, NotIn, Exists, DoesNotExists, Gt, Lt**|
|The field value will be parsed as integer when **Gt, Lt** operators are used _(Gt - Greater Than, Lt - Less Than)_|



**Reference** - <br>
https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes-using-node-affinity/<br>
https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#node-affinity<br>
https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity<br>
https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#operators<br>