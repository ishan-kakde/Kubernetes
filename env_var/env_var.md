|**summary**|
|:------|
|When you create a Pod, you can set environment variables for the containers that run in the Pod. To set environment variables, include the **env** or **envFrom** field in the configuration file.|
|**env** allows you to set environment variables for a container, specifying a value directly for each variable that you name|
|**envFrom** allows you to set environment variables for a container by referencing either a **ConfigMap** or a **Secret**| 
|When you use envFrom, all the key-value pairs in the referenced ConfigMap or Secret are set as environment variables for the container|


**Reference** - <br>
https://kubernetes.io/docs/tasks/inject-data-application/define-environment-variable-container/<br>
https://kubernetes.io/docs/reference/kubectl/generated/kubectl_set/kubectl_set_env/<br>
