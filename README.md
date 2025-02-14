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
## below is wroked for Azure application Gateway
```
kubectl apply -f aks-hello-deployment.yaml

homelab#kubectl.exe get pods
NAME                         READY   STATUS    RESTARTS   AGE
aks-hello-7d77db67d5-p7pbr   1/1     Running   0          2m50s
aks-hello-7d77db67d5-vpdjn   1/1     Running   0          2m50s


homelab#kubectl.exe get svc
NAME                TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)   AGE
aks-hello-service   ClusterIP   10.0.147.136   <none>        80/TCP    3m2s
kubernetes          ClusterIP   10.0.0.1       <none>        443/TCP   79m



homelab#kubectl.exe get ing
NAME                CLASS    HOSTS   ADDRESS         PORTS   AGE
aks-hello-ingress   <none>   *       <Azure Appgateway IP >   80      3m6s
```
## How to attch Azure ACR to AKS cluster
```
az aks update -n jnrlabs-medplum -g jnrlabs-medplum-rg  --attach-acr devacr
```
