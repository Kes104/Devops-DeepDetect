# **DevOps-DeepDetect**

### **ML Deployment & CI/CD Automation for Deepfake Detection**

DevOps-DeepDetect is a **DevOps & MLOps–focused project** that demonstrates how to **containerize, deploy, and automate the lifecycle of a machine learning inference service** using **Docker, Kubernetes, and Jenkins**.

The project deploys an **AI-powered deepfake image detection model** as a scalable inference API and automates its build, test, and deployment using CI/CD pipelines.

---

## **Project Overview**

Deepfake detection models are often difficult to reliably deploy and maintain in production.
This project addresses that problem by implementing:

* Automated **CI/CD pipelines**
* **Containerized ML inference services**
* **Kubernetes-based orchestration**
* Rollback and monitoring mechanisms for **model reliability**

The focus is on **deployment and automation**, not model training.

---

## **Architecture Highlights**

* ML inference served via **FastAPI (Python)**
* Dockerized services for consistent runtime environments
* CI/CD pipelines implemented using **Jenkins**
* Kubernetes used for **container orchestration, scaling, and fault tolerance**
* Automated testing, health checks, and rollback strategies

---

## **Tech Stack**

### **MLOps / DevOps**

* **Docker** – Containerization of ML inference service
* **Kubernetes** – Container orchestration and scaling
* **Jenkins** – CI/CD pipeline automation

### **Backend & ML**

* **FastAPI (Python)** – Model inference API
* **Deep Learning Model** – Deepfake image detection

### **Supporting Tools**

* Git & GitHub – Version control
* REST APIs – Model serving

---

## **Key Features**

✅ Automated CI/CD pipeline for ML deployment
✅ Containerized ML inference service using Docker
✅ Kubernetes-based deployment and scaling
✅ Automated testing and health checks
✅ Rollback strategies for failed deployments
✅ Versioned model and container releases
✅ End-to-end MLOps workflow from code commit to production

---

## **CI/CD Pipeline Workflow**

1. Developer pushes code to GitHub
2. Jenkins pipeline is triggered
3. Automated tests are executed
4. Docker image is built and tagged
5. Image is pushed to container registry
6. Kubernetes deployment is updated
7. Health checks validate the deployment
8. Automatic rollback occurs if failures are detected

---

## **Model Handling**

* The deepfake detection model is **trained externally** (training code provided separately).
* The project focuses on **serving the trained model**, not training it.
* Model artifacts are loaded into the FastAPI inference service at deployment time.

---

## **Installation & Local Setup**

### **Clone the repository**

```bash
git clone https://github.com/naik-shashank/devops-deepdetect.git
cd devops-deepdetect
```

---

### **Run ML Inference API (FastAPI)**

```bash
cd Model_Api
pip install -r requirements.txt
uvicorn main:app --reload
```

---

### **Build & Run with Docker**

```bash
docker build -t deepdetect-inference .
docker run -p 8000:8000 deepdetect-inference
```

---

### **Kubernetes Deployment**

```bash
kubectl apply -f k8s/
kubectl get pods
kubectl get services
```

---

## **Project Goals**

* Demonstrate **real-world ML deployment practices**
* Apply **DevOps principles to machine learning systems**
* Ensure reliable, repeatable, and scalable model serving
* Bridge the gap between **ML experimentation and production deployment**

---

## **Future Enhancements**

* Add Prometheus & Grafana for monitoring
* Canary deployments for model versioning
* Integration with model registry (MLflow)
* Cloud-based Kubernetes deployment (EKS/GKE)

---

## **Contributors**

This is a **group project** developed as part of academic learning, with a primary focus on:

* CI/CD pipeline design
* Containerization
* Kubernetes-based deployment
* MLOps best practices

---

## **License**

MIT License

---
