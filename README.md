# Infra

Kubernetes configuration for the chat-system microservices.

## Technologies

* Kubernetes
* Minikube
* Docker
* RabbitMQ

## Services

* BFF
* Auth Service
* User Service
* Message Service
* Bot Service
* RabbitMQ

## Run

```bash
minikube start

minikube docker-env --shell powershell | Invoke-Expression

docker build -t auth-service:latest ../auth-service
docker build -t user-service:latest ../user-service
docker build -t message-service:latest ../message-service
docker build -t bot-service:latest ../bot-service
docker build -t bff:latest ../bff

kubectl apply -f k8s/

minikube service bff -n chatapp
```

## Verify

```bash
kubectl get pods -n chatapp

kubectl get svc -n chatapp
```
