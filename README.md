## Nginx Ingress Controller in Azure Kubernetes Services.
## source: https://learn.microsoft.com/en-us/azure/aks/ingress-basic?tabs=azure-cli
##
## Azure Application Gateway Load Balancer - 
Part- 1 https://www.youtube.com/watch?v=6b--xLKOqqA&list=PLWgk5rA0Qxea4mwYsrZ8SPXRxD90MnAUR&index=6
Part- 2 https://www.youtube.com/watch?v=x_Rr1Fw2jck&t=540s
Part-3 https://www.youtube.com/watch?v=YMWXxODAmSk


![image](https://github.com/jniranjanreddy/azure-AKS/assets/83489863/42087d97-7c5e-43e9-b263-1d8435886273)

```
NOTW: This is the ingress class name

root@nginx02:/myworkspace/azure-AKS/nginx-ingress/hello-world# k get ingressclass
NAME                                 CONTROLLER                                 PARAMETERS   AGE
webapprouting.kubernetes.azure.com   webapprouting.kubernetes.azure.com/nginx   <none>       154m
```
