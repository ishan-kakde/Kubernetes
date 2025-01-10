# Kubernetes

**HomeBrew** - is macOS package manager<br>
Follow installation steps here - https://brew.sh<br>
Ensure to execute commands under Next steps to add HomeBrew to path - <br>
<img width="920" alt="image" src="https://github.com/user-attachments/assets/bad9e7af-02c0-4f30-8252-e505fd492263" /><br>

HomeBrew enables analytics by default, you may opt out analytics by following instructions here - <br>
https://docs.brew.sh/Analytics<br>
Verify installation - **_brew --version_** <br>


**Install Docker desktop** -

https://docs.docker.com/desktop/setup/install/mac-install/<br>
https://docs.docker.com/desktop/setup/install/windows-install/

once Docker Desktop is installed, validate the installation by running below commands in terminal - 

**_docker version_**  (verify both client and server)<br>
**_docker ps_**<br>

<img width="750" alt="docker_install" src="https://github.com/user-attachments/assets/65322ad5-7c05-4006-81e8-ba87f20ad523" />
<br>

Docker desktop by default installs kubectl CLI, can be verified by using below command - 

**_kubectl version_** (checks both client and server/cluster) <br> 

<img width="836" alt="kubectl_version" src="https://github.com/user-attachments/assets/d1c694b6-190d-4d2b-af85-3e0e24a63876" />


notice the response - The connection to the server localhost:8080 was refused - did you specify the right host or port? This is because the Kubernetes cluster is not available.

This error message do not appear on using the same command with --client flag

**_kubectl version --client_** (checks only for client)

<img width="639" alt="kubectl_version_client" src="https://github.com/user-attachments/assets/08243c8b-7125-4c08-9093-3166d49a7861" />
 
**_kubectl cluster-info_** (checks for both server/cluster)<br>

<img width="841" alt="cluster-info" src="https://github.com/user-attachments/assets/62760150-fba5-46ea-aab3-f183f125f74a" />

***

**Install Kubernetes CLI** - 

Kubernetes CLI can be installed separately.

Below are brew commands - 

**_brew install kubectl_** or<br> **_brew install kubernetes-cli_**

verify installation using **_kubectl version --client_**


***

**Install Kubernetes Cluster** 

A Kubernetes cluster can be enabled from Docker desktop under settings > kubernetes

<br>

<img width="984" alt="enable-k8s-cluster" src="https://github.com/user-attachments/assets/e8b0df7b-729e-4079-b3f2-683c5d6d4c39" />

<br>

once enabled, run below commands to verify - 

**_kubectl version_** <br>
**_kubectl get service_** <br>
**_kubeclt cluster-info_** <br>

<br>
<img width="853" alt="verify_cluster1" src="https://github.com/user-attachments/assets/05a8e594-4f7d-4d29-8107-cdb5871902ec" />

<br>
<br>

Or cluster can be installed separately using minikube. Minikube is a local Kubernetes cluster - 

**_brew install minikube_**

![image](https://github.com/user-attachments/assets/64e11fc5-5f13-4a68-b12a-7db6a000881a)

once installed start minikube by assigning the driver which can be **docker, virtualBox, etc**

**_minikube start --driver=docker_**


<br>
<br>
<br>

**References** - <br>
_Installation_ - https://kubernetes.io/docs/tasks/tools/<br>
_Kubernetes Tutorial_ - https://kubernetes.io/docs/tutorials/kubernetes-basics/<br>
_Minikube Install_ - https://minikube.sigs.k8s.io/docs/start/?arch=%2Fmacos%2Fx86-64%2Fstable%2Fbinary+download<br>
_Minikube Driver_ - https://minikube.sigs.k8s.io/docs/drivers/<br>
_Minikube Tutorial_ - https://kubernetes.io/docs/tutorials/hello-minikube/<br>


