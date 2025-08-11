# 🚀 Kubernetes Minikube Deployment with Docker🐳📦

This project demonstrates how to deploy and manage applications using Kubernetes locally via Minikube. It includes a custom Docker image.

---

## 📦 Tools Used

- 🧱**Minikube**
- 🛠️**Kubernetes**
- 🐳**Docker**

---

## 🚀 Setup Instructions
- Minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.

- Minikube requires minimum of 2 CPUs or more and 2GB of free memory.

- **Follow the official Docker and Minikube installation guides linked below for setup instructions.**
<p align="left"> <a href="https://docs.docker.com/engine/install/" target="_blank"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Badge" /> </a> <a href="https://minikube.sigs.k8s.io/docs/start/?arch=%2Flinux%2Fx86-64%2Fstable%2Fbinary+download" target="_blank"> <img src="https://img.shields.io/badge/Minikube-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Minikube Badge" /> </a> </p>

### Make sure Docker is running and Minikube is properly installed.

---
### 1. Docker Setup
- Install Docker and pull docker image from dockerhub (or build Docker image)
 ```bash
docker pull <docker-hub-username/image-name>
```
### 2. Start Minikube
```bash
minikube start
```
### 3. Load Local Docker Image into Minikube
```bash
minikube image load <image-name:tag>
```
### 4. Apply Kubernetes Manifests
- Make sure you update your docker <**image:tag**> in **deployment.yaml** file
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
### 5. Verify Pod and Services
```bash
kubectl get pods
kubectl get services
```
### 6. Scale Deployments
- To increase the number of pods which improves the **performance, availability** and **reliability** of your application.
```bash
kubectl scale deployment java-app-deployment --replicas=3
kubectl get pods
```
### 7. Check Logs and Describe
```bash
kubectl logs <pod-name>
kubectl describe pod <pod-name>
```

---
## 📤 Outputs
- **Displaying the output of Kubernetes Manifests**
![image alt](https://github.com/Pranaykokkonda/kubectl-task5/blob/4da782921a57a24d368be176378c60a43984abb4/01-Kubernetes-Apply.JPG)
- **Displaying the output of Kubernetes pods and logs**
![image alt](https://github.com/Pranaykokkonda/kubectl-task5/blob/4da782921a57a24d368be176378c60a43984abb4/02-kubectl-pods-logs.jpg)
- **Displaying the output of Kubernetes services**
![image alt](https://github.com/Pranaykokkonda/kubectl-task5/blob/4da782921a57a24d368be176378c60a43984abb4/03-kubectl-get-services.jpg)
- **Displaying the output of Kubernetes scale deployment**
![image alt](https://github.com/Pranaykokkonda/kubectl-task5/blob/4da782921a57a24d368be176378c60a43984abb4/04-kubectl-scale-deployment.jpg)

---

