|**commands**|
|:-------|
|kubectl create serviceaccount [sa-name]|
|kubectl get serviceaccounts|
|kubectl describe serviceaccount [sa-name]|
|kubectl exec -it [pod-name] -- ls /var/run/secrets/kubernetes.io/serviceaccount  _(location where token is stored)_|
|kubectl exec -it [pod-name] -- cat /var/run/secrets/kubernetes.io/serviceaccount/token  _(to view the token, **decode** token at **jwt.io** and validate service account and pod information)_|
|kubectl create token [sa-name] _(version 1.24 to 1.26 prevented kubernetes to auto create token, this command is used to create token manually)_|


|**summary**|
|:------|
|User accounts are for human whereas service accounts are for processes |
|User account provides unique identity to entities in Kubernetes cluster|
|Every namespace has a default service account|
|If a default service account is deleted, the controlplane replaces it with new one|
|When a new pod is created, it is assigned with default service account & token is mounted as volume mount|
|Describe pod and verify Service Account, Mounts, volumes. _(run exec commands from commands section to view token)_ |
|default service account can be overriden by including **serviceAccountName** property in pod definition file|


**Reference** - <br>
https://kubernetes.io/docs/concepts/security/service-accounts/
