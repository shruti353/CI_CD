# Iris Flower Classification – MLOps Project (Docker Swarm)

This project demonstrates an **end-to-end MLOps pipeline** for the Iris flower classification problem.  
The solution covers **model training, containerization, deployment using Docker Swarm, and API testing**.

---

## 📌 Project Overview

- **Dataset**: Iris Dataset (UCI Machine Learning Repository)
- **Model**: RandomForestClassifier
- **API Framework**: Flask
- **Containerization**: Docker
- **Orchestration**: Docker Swarm
- **Language**: Python
- **Deployment**: GitHub Container Registry (GHCR)

The trained ML model is exposed as a **REST API** and deployed with **multiple replicas** using Docker Swarm.


---

## ⚙️ Requirements

- Python 3.10+
- Docker & Docker Desktop
- Docker Swarm initialized
- GitHub account (for container registry)

---

## 🚀 Steps to Run the Project

### 1️⃣ Create & Activate Virtual Environment

python -m venv venv
venv\Scripts\activate

### 2️⃣ Install Dependencies
pip install -r requirements.txt

### 3️⃣Train the Model
python train.py

### 4️⃣ Build Docker Image
docker build -t ghcr.io/<your-username>/iris-ml-app:latest .

### 7️⃣ Deploy the Application using Docker Swarm
docker stack deploy -c swarm_stack.yml iris_stack

### 8️⃣ Verify Running Services
docker stack services iris_stack

## 🎓 Academic Information

Course: MSc Data Science – Semester IV

Subject: MLOps / CI-CD

Project Type: Mini Project / Practical Implementation

Date: January 2026

## Conclusion

This project demonstrates how a machine learning model can be taken from training to production deployment using modern MLOps practices.
Docker Swarm ensures scalability and reliability, while Flask provides a lightweight API layer for inference.