|**summary**|
|:------|
|When you create a Pod, you can define a command and arguments for the containers that run in the Pod|
|To define a command, include the command field in the configuration file|
|To define arguments for the command, include the args field in the configuration file|
|The command and arguments that you define cannot be changed after the Pod is created|
|The command and arguments that you define in the configuration file override the default command and arguments provided by the container image|
|If you define args, but do not define a command, the default command is used with your new arguments.|
|The **command** field corresponds to **ENTRYPOINT**, and the **args** field corresponds to **CMD** in some container runtimes.|


**Reference** - <br>
https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/