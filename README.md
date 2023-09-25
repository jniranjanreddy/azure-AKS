# azure-AKS
![aks](https://user-images.githubusercontent.com/83489863/162898113-c5d6baa2-e813-47bb-be07-f43833afe0ca.JPG)


```
az account set --subscription 80ea84e8-afce-xxxxxxx-xxxxxxxxxx


az aks get-credentials --resource-group 1-7e90c6e4-playground-sandbox --name aksdemo01

# List all deployments in all namespaces
kubectl get deployments --all-namespaces=true

# List all deployments in a specific namespace
# Format :kubectl get deployments --namespace <namespace-name>
kubectl get deployments --namespace kube-system

# List details about a specific deployment
# Format :kubectl describe deployment <deployment-name> --namespace <namespace-name>
kubectl describe deployment my-dep --namespace kube-system

# List details about a specific deployment
# Format :kubectl describe deployment <deployment-name> --namespace <namespace-name>
kubectl describe deployment my-dep --namespace kube-system

# Get logs for all pods with a specific label
# Format :kubectl logs -l <label-key>=<label-value>
kubectl logs -l app=nginx --namespace kube-system

niranjan@Azure:~$ az aks get-credentials --resource-group webserver_group --name aks-demo
Merged "aks-demo" as current context in /home/niranjan/.kube/config
```
## How to connect to kubernetes nodes in node pools
```
NAME                                STATUS   ROLES   AGE    VERSION   INTERNAL-IP   EXTERNAL-IP   OS-IMAGE  KERNEL-VERSION      CONTAINER-RUNTIME
aks-nodepool1-37663765-vmss000000   Ready    agent   166m   v1.25.6   10.224.0.33   <none>        Ubuntu 22.04.2 LTS               5.15.0-1039-azure   containerd://1.7.1+azure-1
aks-nodepool1-37663765-vmss000001   Ready    agent   166m   v1.25.6   10.224.0.4    <none>        Ubuntu 22.04.2 LTS               5.15.0-1039-azure   containerd://1.7.1+azure-1
aksnpwin000000                      Ready    agent   160m   v1.25.6   10.224.0.62   <none>        Windows Server 2022 Datacenter   10.0.20348.1787     containerd://1.6.21+azure

kubectl debug node/aks-agentpool-27538887-vmss000000 -it --image=mcr.microsoft.com/dotnet/runtime-deps:6.0
```
## How to Delete AKS Cluster.
```
az aks delete --resource-group my-RG --name aks-clustername
Are you sure you want to perform this operation? (y/n): y
 \ Running ..
```
