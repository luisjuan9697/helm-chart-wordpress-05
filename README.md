# Overview
Helm Chart to install k8s wordpress deployment


# Features
- Uses Longhorn, MetalLB, NGINX ingress, Cert-Manager, and ns secrets


# Quickstart
```
kubectl create namespace nswordpress-helm

kubectl create secret generic mysql-password-f547bhm8mc --from-literal=password=Mysql.Root2021@ -n nswordpress-helm
kubectl create secret generic mysql-user-4t5mcf8dkm --from-literal=username=userwp -n nswordpress-helm
kubectl create secret generic mysql-user-password-9m7k5b4k2m --from-literal=passworduser=Mysql.User2021@ -n nswordpress-helm
kubectl create secret generic mysql-database-4f74mgddt5 --from-literal=database=multitenant_wp -n nswordpress-helm

helm create 
helm install my-wordpress-helm ./ --namespace nswordpress-helm
```
