# Infra

Kubernetes configuration for the chat-system microservices.

## Technologies

- Kubernetes
- Minikube
- Docker
- RabbitMQ

## Services

- BFF
- Auth Service
- User Service
- Message Service
- Bot Service
- RabbitMQ

## Run

```bash
minikube start

kubectl apply -f k8s/

minikube service bff -n chatapp