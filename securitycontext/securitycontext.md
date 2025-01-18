|**commands**|
|:-------|
|kubectl exec -it [podname] -- whoami _(command to find user within pod)_|
|kubectl get pod [pod-name] -o yaml > pod-def.yaml _(add securityContext to the definition file and replace pod)_|


|**summary**|
|:------|
|security context defines privileges and access control settings for a pod or container|
|security context can be applied at pod level or container level or at both|
|security context provided at pod level applies to all container|
|security context at provided at container level overrides security context at pod level|
|field **runAsUser** - The UID to run the entrypoint of the container process|
|field **capabilities** - The capabilities to add/drop when running containers|
|If you want to run pod/container as root user then no need to add securityContext in defintion file, root is by default|

**Reference** - <br>
https://kubernetes.io/docs/tasks/configure-pod-container/security-context/<br>
https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.32/#securitycontext-v1-core<br>