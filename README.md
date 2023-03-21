## How to run (Mac)

1. Start Docker Desktop application
2. Run `minikube start`
3. In a new terminal run `minikube tunnel`
4. Run `minikube addons enable ingress`
5. Run `kubectl apply -k .`
6. Wait for ingress address, check using `kubectl get ing -A`
7. Run `curl 127.0.0.1`
