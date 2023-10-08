## Nginx Ingress Controller in Azure Kubernetes Services.
## source: https://learn.microsoft.com/en-us/azure/aks/ingress-basic?tabs=azure-cli
## 

![image](https://github.com/jniranjanreddy/azure-AKS/assets/83489863/42087d97-7c5e-43e9-b263-1d8435886273)

```
NOTW: This is the ingress class name

root@nginx02:/myworkspace/azure-AKS/nginx-ingress/hello-world# k get ingressclass
NAME                                 CONTROLLER                                 PARAMETERS   AGE
webapprouting.kubernetes.azure.com   webapprouting.kubernetes.azure.com/nginx   <none>       154m
```