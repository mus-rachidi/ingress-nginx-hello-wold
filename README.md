# ingress-nginx-hello-wold

## start 

Minikube will start a Kubernetes cluster with two nodes using the Docker driver, and it will be associated with the "cluster-test-1" profile.


```
minikube start --nodes 2 --profile cluster-test-1 --driver=docker
```


```
minikube status --profile cluster-test-1
minikube ip --profile cluster-test-1
minikube ssh --profile cluster-test-1
```

```
minikube addons enable ingress --profile cluster-test-1
minikube addons list  --profile cluster-test-1
```

```
kubectl apply -f kubectl apply -f nginx-deployment.yaml
kubectl apply -f nginx-service.yaml 
kubectl apply -f hello-world-ingress.yaml
```

```
kubectl get all 
kubectl get ingress
```


curl -H "Host: hello-world.local" http://192.168.67.2
or 
sudo vim /etc/hosts
curl hello-world.local


