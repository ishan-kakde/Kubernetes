|**commands**||
|:-------|:------|
|add taint| kubectl taint nodes node1 key1=value1:NoSchedule |
|remove taint| kubectl taint nodes node1 key1=value1:NoSchedule-|
|add toleration|toleration can be added to a Pod through the pod-definition.yaml file|

|**summary**|
|:------|
|**Taints** are applied to nodes. Taints makes a node to repel a set of pods|
|**Tolerations** are applied to pods. Tolerations allow the scheduler to schedule pods with matching taints, but does not guarantee scheduling|
|Taints and tolerations work together to ensure that pods are not scheduled onto inappropriate nodes|
|There are three types of taint effects - **NoExecute, NoSchedule, PreferNoSchedule**|
|**NoExecute** affects pods that are already running on the node<br> - Pods that do not tolerate the taint are evicted<br> - Pods that are tolerant to taint remain bound forever<br> - Pods that are tolerant to taint & specified with tolerationSeconds remain bound for the specified amount of time |
|**NoSchedule** means no new Pod can get schedule on the node unless it has a matching toleration  |
|**PreferNoSchedule** Scheduler will try to avoid placing a Pod that does not tolerate the taint on the node, but is not **guranteed**|
|A node may have mulitple taints and a pod may have multiple tolerations|
|Tolerations in a Pod definition has four attributes - **key, operator, value, effect**  |
|Operator can have two values - **Equal** or **Exists**. The default value of the operator is  **Equal**|
| * A toleration with operator **Equals** matches a taint if a key, value & effect is matching (value must be specified) |
| * A toleration with operator **Exists** matches a taint if a key and effect is matching (**no value** should be specified) |

**Reference** - <br>
https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration<br>
