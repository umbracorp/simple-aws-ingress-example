# Simple AWS Ingress Example

This example is to facilitate testing of AWS EKS ingress with AWS ALB.

## Prerequisites

- kubectl installed.
- AWS EKS cluster exists.
- kubectl configured to use the AWS EKS.
- The aws-load-balancer-controller (https://aws.github.io/eks-charts) helm chart must be installed to the cluster.

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

## Test

You should be able to access the path _host/hello-world_ on the cluster and see a simple http page displaying "hello-world".

`kubectl get -n hello-world ingress/hello-world-ingress` should show the external IP of the ingress under the ADDRESS column.
