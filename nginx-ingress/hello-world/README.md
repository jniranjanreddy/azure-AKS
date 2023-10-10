## Source: https://learn.microsoft.com/en-us/azure/aks/ingress-basic?tabs=azure-cli

## how to check through CURL
```
kubectl run -it --rm aks-ingress-test --image=mcr.microsoft.com/dotnet/runtime-deps:6.0 --namespace ingress-basic
apt-get update && apt-get install -y curl

curl -L http://10.224.0.42
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <link rel="stylesheet" type="text/css" href="/static/default.css">
    <title>Welcome to Azure Kubernetes Service (AKS)</title>


curl -L -k http://10.224.0.42/hello-world-two
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <link rel="stylesheet" type="text/css" href="/static/default.css">
    <title>AKS Ingress Demo</title>

```