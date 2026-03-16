# 🚀 Kubernetes Microservices Deployment with Docker

## 📌 Project Overview

This project demonstrates deploying a **cloud-native microservices architecture** using **Docker and Kubernetes**.
Three independent services (**User Service, Product Service, Order Service**) were containerized using Docker and deployed on a **Kubernetes cluster (Minikube)** running on an **AWS EC2 instance**.

The project showcases real-world **DevOps practices** including containerization, service discovery, and scalable deployment.

---

## 🏗 Architecture Diagram
![](/img/Architecture-Diagram.png)
       
---


## 🛠 Technologies Used

* **AWS EC2**
* **Docker**
* **Kubernetes**
* **Minikube**
* **Flask (Python Microservices)**
* **kubectl**
* **NodePort Services**

---

## 📦 Microservices

### 👤 User Service

* Runs on **Port 5000**
* Provides user-related information
* Health check endpoint

Endpoints:

```
/           → Service UI
/users      → List users
/health     → Service health
```

---

### 📦 Product Service

* Runs on **Port 5001**
* Returns product catalog

Endpoints:

```
/           → Service UI
/products   → Product list
/health     → Service health
```

---

### 🧾 Order Service

* Runs on **Port 5002**
* Displays order data

Endpoints:

```
/           → Service UI
/orders     → Order list
/health     → Service health
```
# 🌐 Microservice UI Preview

Each microservice exposes a simple UI page to verify that the service is running successfully.
These pages were built using **Flask + HTML + CSS**.

---

## 👤 User Service UI

Runs on **Port 5000**

Access:

```
http://EC2-IP:5000
```

Description:

Displays a dashboard indicating that the **User Microservice is active** and running inside a Docker container.

Example Output:

```
👤 User Service
Microservice Running Successfully
Docker • Kubernetes • DevOps
Status: ACTIVE
```

---

## 📦 Product Service UI

Runs on **Port 5001**

Access:

```
http://EC2-IP:5001
```

Description:

Displays product service status and confirms that the **Product Microservice is running correctly**.

Example Output:

```
📦 Product Service
Handles product catalog
Docker • Kubernetes • DevOps
Status: ACTIVE
```

---

## 🧾 Order Service UI

Runs on **Port 5002**

Access:

```
http://EC2-IP:5002
```

Description:

Displays order management service status and confirms the **Order Microservice deployment**.

Example Output:

```
🧾 Order Service
Handles customer orders
Docker • Kubernetes • DevOps
Status: ACTIVE
```

---

# 📸 UI Screenshots

Example section:

### User Service

![User Service UI](/img/user-service.png)

### Product Service

![Product Service UI](/img/product-service.png)

### Order Service

![Order Service UI](/img/order-service.png)

---

## 🐳 Docker Containerization

Each microservice was containerized using Docker.

Example build command:

```
docker build -t user-service .
docker build -t product-service .
docker build -t order-service .
```

---

## ☸ Kubernetes Deployment

All services were deployed using **Kubernetes Deployment and Service YAML manifests**.

Example deployment:

```
kubectl apply -f k8s/
```

Check pods:

```
kubectl get pods
```

Check services:

```
kubectl get svc
```

---

## 🌐 Access Services

After deployment, services are exposed using **NodePort**.

| Service         | NodePort |
| --------------- | -------- |
| User Service    | 30001    |
| Product Service | 30002    |
| Order Service   | 30003    |

Access using:

```
http://MINIKUBE-IP:30001
http://MINIKUBE-IP:30002
http://MINIKUBE-IP:30003
```

Find Minikube IP:

```
minikube ip
```

---

## 📸 Screenshots

### Kubernetes Pods

![](/img/get-pod.png)

### Kubernetes Services

![](/img/get-svc.png)

### PV

![](/img/get-pv.png)

### PVC

![](/img/get-pvc.png)

### HPA (Autoscalling)

![](/img/HPA.png)

---

## ⚙️ DevOps Skills Demonstrated

* Microservices Architecture
* Docker Containerization
* Kubernetes Deployments
* Service Discovery
* NodePort Networking
* Cloud Deployment on AWS

---

## 🎯 Key Learning Outcomes

* Deploying containerized applications on Kubernetes
* Managing multiple microservices
* Kubernetes networking using Services
* Scaling and managing pods
* Cloud-native application architecture

---

## 🔮 Future Improvements

* Implement **Horizontal Pod Autoscaler (HPA)**
* Add **CI/CD pipeline**
* Use **Docker Hub or ECR for image registry**
* Deploy on **AWS EKS**

---

## 👨‍💻 Author

**Vivek Chopade**

- DevOps | Cloud | AWS | Kubernetes

GitHub:
https://github.com/chopadevivek07
