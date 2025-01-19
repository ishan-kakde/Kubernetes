|**commands**||
|:-------|:--------|
|get label|kubectl get nodes --show-labels|
|create label|kubectl label nodes [node-name] [lable-key]=[label-value]|
|pod with node info|kubectl get pods -o wide|


|**summary**|
|:------|
|This page shows how to assign a Pod to a particular node in a Kubernetes cluster|
|**nodeSelector** or **nodeName** are the feilds used to assign a pod to a particular node|
|**nodeSelector** is the simplest recommended form of node selection constraint<br> Add the nodeSelector field to pod definition and specify the label of the node where you want the pod to run|
|**nodeName** is more direct form of node selection than affinity or nodeSelector|
|Using nodeName disallows using nodeSelector, affinity or anti-affinity rules|
|**Disadvantages** of nodeName<br> - If the named node does not exist, then pod will not run<br> - If named node does not have enough resource it will fail the pod with reason. ex. out of cpu or memory<br> - node names are not always predictable or stable|
|Review pod definition files in folder node_selector|


**Reference** - <br>
https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes<br>
https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#nodename<br>