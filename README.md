# Fusion Links Final Project – Part 1

## 🐳 Docker + Kubernetes (Minikube)

This section covers containerizing a simple python application with Docker, and deploying it to a local Kubernetes cluster using Minikube.

---

---

### 1️ Build the Docker Image
```bash
docker build -t python-app:1.0 .
```

### 2 Run and test locally
```
docker run -p 5000:5000 python-app:1.0
```
This will test the app locally on your browser
![See here](<./tests/local_test.png>)
### 3 Deploy on Minikube
```
minikube start
```
Deploy
```
kubectl apply -f deployment.yaml
```
Access the app
```
minikube service python-app-service
```
This will open the app in your browser. This is how it should look ![like](<./tests/deploy_test.png>)