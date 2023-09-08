# ingress-nginx-hello-wold
minikube start --nodes 2 --profile cluster-test-1 --driver=docker

minikube status --profile cluster-test-1
minikube ip --profile cluster-test-1
minikube ssh --profile cluster-test-1

minikube addons enable ingress --profile cluster-test-1
minikube addons list  --profile cluster-test-1

kubectl apply -f hello-world-ingress.yaml
kubectl apply -f nginx-service.yaml 
kubectl apply -f hello-world-ingress.yaml
 
kubectl get all 
kubectl get ingress

curl hello-world.local