|commands|
|:-------|
|kubectl create serviceaccount [sa-name]|
|kubectl get serviceaccounts|
|kubectl describe serviceaccount [sa-name]|


|summary|
|:------|
|user accounts are for human whereas service accounts are for processes |
|user account provides unique identity to entities in Kubernetes cluster|
|every namespace has a default service account|
|If a default service account is deleted, the controlplane replaces it with new one|

Reference - <br>
https://kubernetes.io/docs/concepts/security/service-accounts/