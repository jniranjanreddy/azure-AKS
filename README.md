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

