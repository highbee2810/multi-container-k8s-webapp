# multi-container-k8s-webapp
# Multi-Container Kubernetes Web App

This project demonstrates a multi-container Pod running an NGINX web server with a sidecar logger container. It uses persistent volumes to store data and a ConfigMap to manage NGINX configuration.

## 🧰 Technologies Used
- Kubernetes (Minikube)
- ConfigMaps
- PersistentVolumeClaim
- Sidecar container pattern
- NodePort Service

## 📦 Project Structure
- `k8s/`: Kubernetes YAML files
- `html/`: Web content served by NGINX
- `images/`: Screenshots

## 🚀 Getting Started

```bash
minikube start
kubectl apply -f k8s/configmap.yaml
kubectl apply -f k8s/pvc.yaml
kubectl apply -f k8s/pod.yaml
kubectl apply -f k8s/service.yaml
minikube service webapp-service
