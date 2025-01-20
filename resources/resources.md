|**commands**|
|:-------|

|**summary**|
|:------|
|When you specify a Pod, you can optionally specify how much of each resource a container needs|
|The most common resources to specify are CPU and memory (RAM); there are others|
|When you specify the resource **request** for containers in a Pod, the kube-scheduler uses this information to decide which node to place the Pod on|
|When you specify a resource **limit** for a container, the kubelet enforces those limits so that the running container is not allowed to use more of that resource than the limit you set|
|The kubelet also reserves at least the request amount of that system resource specifically for that container to use|
|If the node where a Pod is running has enough of a resource available, it's possible (and allowed) for a container to use more resource than its request for that resource specifies.|
|Limits are a different story. Both cpu and memory limits are applied by the kubelet (and container runtime), and are ultimately enforced by the kernel|
|The behavior of cpu and memory limit enforcement is slightly different.|
|**cpu** limits are enforced by CPU throttling. When a container approaches its cpu limit, the kernel will restrict access to the CPU corresponding to the container's limit. Thus, a cpu limit is a hard limit the kernel enforces. Containers may not use more CPU than is specified in their cpu limit|
|**memory** limits are enforced by the kernel with out of memory (OOM) kills. When a container uses more than its memory limit, the kernel may terminate it. However, terminations only happen when the kernel detects memory pressure. Thus, a container that over allocates memory may not be immediately killed. This means memory limits are enforced reactively. A container may use more memory than its memory limit, but if it does, it may get killed|
|CPU and memory are collectively referred to as compute resources, or resources.|
|By default there is no request or limit set by Kubernetes, that means a pod/container may use as much resources as required on a node|
|resource and limits can be applied to each container within a pod or at pod level|
|Pod level resource specifications is under **development stage - v1.32 [alpha]** and **not** enabled by default|
|For each container, you can specify resource limits and requests, including the following<br> - spec.containers[].resources.**limits**.cpu<br> - spec.containers[].resources.**limits**.memory<br> - spec.containers[].resources.**requests**.cpu<br> - spec.containers[].resources.**requests**.memory|
|For a Pod(**under development**), you can specify resource limits and requests for CPU and memory by including the following<br> - spec.resources.**limits**.cpu<br>- spec.resources.**limits**.memory<br>- spec.resources.**requests**.cpu<br>- spec.resources.**requests**.memory<br> |


**Reference** - <br>
https://kubernetes.io/docs/concepts/configuration/manage-resources-containers<br>
https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/#meaning-of-cpu<br>
https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/#meaning-of-memory<br>

