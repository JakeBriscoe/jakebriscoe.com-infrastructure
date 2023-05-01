## How to run (Mac)

1. Start Docker Desktop application
2. Run `minikube start`
3. In a new terminal run `sudo minikube tunnel` root privilege are needed for protected ports 80, 443
4. Run `minikube addons enable ingress`
5. Run `kubectl apply -k apps/environments/dev/`
6. Wait for ingress address, check using `kubectl get ing -A`
7. Run `curl 127.0.0.1`

### To connect to database

1. In a new terminal run `kubectl port-forward service/postgres-service 5432:5432 -n dev`
2. Run `psql -h 127.0.0.1 -p 5432 -U myuser -d mydatabase`
