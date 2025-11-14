# 🚀 Project: MLflow Experiment Tracking Pipeline  
**Part of the “AI & MLOps Zero to Hero (180-Day Challenge)” by [Arbind Kumar Mahato](https://www.linkedin.com/in/arbindmahato/)**  

---

## 🧑‍💻 Author Details

**👤 Name:** Arbind Kumar Mahato  
**💼 Current Role:** Cloud & DevOps Engineer | Workmates Core2Cloud | Kolkata, India  
**🌐 Experience:** 8+ Years (System Admin → Cloud Engineer → DevOps → MLOps Transition)  
**🎓 Background:** B.Com Graduate + Diploma in Computer Application (2010)  
**🎥 Content Creator:** [Tech Mahato YouTube Channel (8K+ Subscribers)](https://www.youtube.com/techmahato)  
**🔗 LinkedIn:** [linkedin.com/in/arbindmahato](https://www.linkedin.com/in/arbindmahato)  
**📸 Instagram:** [@techmahato](https://www.instagram.com/techmahato)  
**🌐 Website:** [techmahato.com](https://techmahato.com)  

> 📢 Mission: *To empower DevOps professionals to transition into AI & MLOps through real-world, cloud-native learning projects.*

---

## 📘 About This Project

This project demonstrates how to build an **end-to-end Machine Learning pipeline** with experiment tracking, dataset versioning, and API deployment using modern MLOps tools like **MLflow**, **DVC**, and **FastAPI** — integrated with **AWS S3** for cloud storage and **Terraform** for automated infrastructure.

It is part of my **180-Day AI & MLOps Zero to Hero Challenge**, where I learn, implement, and share every step publicly through GitHub, LinkedIn, and YouTube.

---

## 🎯 Project Objectives

- 🧩 Build a **reproducible ML experiment workflow**
- 📊 Log metrics, parameters & artifacts using **MLflow**
- 📦 Version datasets & models using **DVC**
- ⚙️ Serve trained models via **FastAPI REST API**
- ☁️ Store artifacts on **AWS S3**
- 🏗️ Automate infrastructure provisioning using **Terraform**
- 🔄 Enable CI/CD pipeline via **GitHub Actions**

---

## 🧰 Tech Stack

| Category | Tools |
|-----------|-------|
| Language | Python |
| ML Framework | scikit-learn |
| Experiment Tracking | MLflow |
| Data Versioning | DVC |
| Serving API | FastAPI |
| Infrastructure as Code | Terraform |
| Cloud | AWS (S3, IAM, SageMaker – future) |
| Containerization | Docker |
| CI/CD | GitHub Actions |
| Monitoring | Evidently AI (later phases) |

---

## 🧩 Project Folder Structure

```
project-mlflow-pipeline/
│
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_model_training.ipynb
│   └── 03_experiment_tracking.ipynb
│
├── src/
│   ├── data/           # data loading & preprocessing
│   ├── model/          # training, metrics, artifact saving
│   └── serve/          # FastAPI app for inference
│
├── infra/
│   ├── terraform/      # IaC for S3 & IAM
│   └── scripts/        # helper bash scripts
│
├── Makefile            # automation tasks
├── requirements.txt    # dependencies
└── README.md           # you are here
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone -b feature/project-mlflow-pipeline https://github.com/techmahato/ai-mlops-zero-to-hero.git
cd ai-mlops-zero-to-hero
```

### 2️⃣ Set Up Environment
```bash
python -m venv venv
source venv/bin/activate   # (or venv\Scripts\activate on Windows)
pip install -r requirements.txt
```

### 3️⃣ Configure Environment Variables
Create a `.env` file for your S3 credentials (use IAM keys with limited access):
```bash
AWS_ACCESS_KEY_ID=<your_access_key>
AWS_SECRET_ACCESS_KEY=<your_secret_key>
MLFLOW_S3_ENDPOINT_URL=https://s3.ap-south-1.amazonaws.com
```

### 4️⃣ Run MLflow Locally
```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root s3://your-bucket-name/mlflow-artifacts
```
Open MLflow UI → [http://localhost:5000](http://localhost:5000)

### 5️⃣ Train and Log Model
```bash
python src/model/train.py
```

### 6️⃣ Run FastAPI Model Server
```bash
uvicorn src.serve.app:app --reload
```
API Endpoint → [http://localhost:8000/predict](http://localhost:8000/predict)

---

## 📦 Example Makefile Commands

```makefile
install:
	pip install -r requirements.txt

train:
	python src/model/train.py

run:
	uvicorn src.serve.app:app --reload

mlflow:
	mlflow ui --port 5000
```

---

## 📈 Learning Outcomes

✅ Understand ML experiment tracking using MLflow  
✅ Manage and version datasets with DVC  
✅ Serve models via REST API with FastAPI  
✅ Deploy artifacts on AWS S3 using Terraform  
✅ Apply DevOps principles to MLOps workflows  
✅ Prepare for real-world MLOps roles and freelancing  

---

## 🌐 Deployment (Future Scope)

| Stage | Tool | Description |
|--------|------|--------------|
| Cloud Infra | Terraform | Provision AWS S3 + IAM Roles |
| Model Training | SageMaker | Move local training to managed service |
| Model Serving | KServe on EKS | Deploy containerized ML models |
| Monitoring | Evidently + Prometheus | Monitor drift & performance |

---

## 🧠  Key Learnings & Insights (From Arbind)

> “As a DevOps engineer transitioning into MLOps, the biggest realization is that **MLOps is 80% engineering and 20% modeling**.  
> The discipline, reproducibility, and automation mindset from DevOps is exactly what modern ML systems need.”  

---

## 📺 Related Content

🎥 YouTube: [Tech Mahato — MLOps Practical Playlist](https://www.youtube.com/techmahato)  
📝 LinkedIn: [Daily Progress Posts](https://www.linkedin.com/in/arbindmahato)  
📸 Instagram: [@techmahato](https://www.instagram.com/techmahato)

---

## 🏁 Challenge Progress Tracker

| Day | Topic | Status |
|-----|--------|---------|
| 25 | MLflow Setup & UI | ✅ |
| 26 | DVC Data Versioning | 🔄 In Progress |
| 27 | FastAPI Deployment | ⏳ Planned |
| 28 | AWS Terraform Infra | ⏳ Planned |

---

## 📊 Sample Results (Will update as progress continues)

| Metric | Value |
|---------|--------|
| Model | RandomForestClassifier |
| Accuracy | 0.941 |
| F1-Score | 0.935 |
| Experiments Logged | 5 |
| Artifacts Stored | 25 MB on S3 |

---

## 🤝 Contributions

This repository is **public and open for learning**.  
If you’re following this challenge, feel free to:
1. Fork the repo  
2. Create your own `feature/` branch  
3. Add improvements or variations  
4. Submit a Pull Request 🚀

---

## 📜 License
This project is licensed under the **MIT License** — free for learning and re-use with credit.

---

## 💬 Connect with Me

👤 **Arbind Kumar Mahato**  
🌐 [techmahato.com](https://techmahato.com)  
💼 [LinkedIn](https://www.linkedin.com/in/arbindmahato)  
📺 [YouTube](https://www.youtube.com/techmahato)  
📸 [Instagram](https://www.instagram.com/techmahato)  
📧 techmahato@gmail.com  

---

> **“Learn in public, build in cloud, and share your story — that’s how engineers grow into leaders.”**

---

### 🏆 Tagline
**“From DevOps to MLOps — One Day, One Project, One Step Closer.”**
