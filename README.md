# deploy-kubernetes-ingress
Deploy nginxinc/kubernetes-ingress controller in GKE cluster

```
kubectl apply -f ns-and-sa.yaml
kubectl apply -f default-server-secret.yaml
kubectl apply -f nginx-config.yaml
kubectl create clusterrolebinding cluster-admin-binding --clusterrole cluster-admin --user $(gcloud config get-value account)
kubectl apply -f rbac.yaml
kubectl apply -f nginx-ingress.yaml
kubectl apply -f loadbalancer.yaml
```
