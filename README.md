# Simple AWS Ingress Example

This example is to facilitate testing of AWS EKS ingress with AWS ALB.

## Deploy

```bash
kubectl create ns hello-world
kubectl apply -n hello-world -f manifests/
```

## Destroy

```bash
kubectl delete -n hello-world -f manifests/
kubectl delete ns hello-world
```
