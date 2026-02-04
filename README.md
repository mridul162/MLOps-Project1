# 🚗 End‑to‑End MLOps Project (Production‑Ready)

> **A complete, industry‑grade MLOps pipeline** demonstrating how real‑world Machine Learning systems are designed, built, deployed, monitored, and continuously delivered using modern tools and cloud infrastructure.

This project is intentionally designed to **impress recruiters, reviewers, and hiring managers** by showcasing **engineering depth**, **cloud readiness**, and **best MLOps practices**.

---

## ✨ Key Highlights

✅ Modular & scalable project structure  
✅ MongoDB Atlas for cloud data ingestion  
✅ Robust logging & exception handling  
✅ Config‑driven data validation & transformation  
✅ Model training, evaluation & versioning  
✅ AWS S3–based model registry  
✅ Dockerized ML application  
✅ CI/CD with GitHub Actions  
✅ Self‑hosted runner on AWS EC2  
✅ Production‑ready prediction pipeline

---

## 🧠 Tech Stack

| Category | Tools |
|-------|------|
| Language | Python 3.10 |
| Data | MongoDB Atlas |
| ML | Scikit‑learn |
| MLOps | Custom pipelines, YAML configs |
| Cloud | AWS (IAM, S3, ECR, EC2) |
| Containerization | Docker |
| CI/CD | GitHub Actions |
| Deployment | EC2 (Self‑hosted runner) |

---

## 📁 Project Structure (High Level)

```
├── app.py
├── demo.py
├── setup.py
├── pyproject.toml
├── requirements.txt
├── constants/
├── src/
│   ├── components/
│   ├── configuration/
│   ├── data_access/
│   ├── entity/
│   ├── aws_storage/
│   ├── utils/
│   └── pipeline/
├── notebook/
├── static/
├── templates/
├── Dockerfile
├── .dockerignore
├── .github/workflows/aws.yaml
└── README.md
```

---

## ⚙️ Environment & Project Setup

### 1️⃣ Project Template
```bash
python template.py
```

### 2️⃣ Local Package Management
- Configured **setup.py** and **pyproject.toml**
- Enables reusable, importable local modules

📘 *Reference:* `crashcourse.txt`

### 3️⃣ Virtual Environment
```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
```

### 4️⃣ Verify Installation
```bash
pip list
```

---

## 🍃 MongoDB Atlas (Cloud Data Layer)

### Setup Steps
- Create MongoDB Atlas project
- Deploy **M0 Free Cluster**
- Create DB user & credentials
- Allow network access: `0.0.0.0/0`
- Obtain Python connection string

### Data Ingestion
- Dataset loaded via Jupyter Notebook
- Stored as **key‑value documents**
- Verified via Atlas UI

```bash
export MONGODB_URL="mongodb+srv://<username>:<password>@..."
```

---

## 🪵 Logging & 🚨 Exception Handling

- Centralized logging system
- Custom exception class
- Tested via `demo.py`
- Enables easy debugging & traceability

---

## 📊 EDA & Feature Engineering

- Dedicated Jupyter notebooks
- Data understanding & feature preparation
- Clean separation from production code

---

## 🔄 Data Ingestion Pipeline

- MongoDB connection abstraction
- Config‑driven ingestion
- Artifact‑based outputs
- Fully modular pipeline design

Triggered via:
```bash
python demo.py
```

---

## 🧪 Data Validation

- Schema‑based validation (`schema.yaml`)
- Ensures:
  - Column presence
  - Data types
  - Drift detection readiness

---

## 🔧 Data Transformation

- Feature scaling & preprocessing
- Reusable estimator architecture
- Clean separation of concerns

---

## 🤖 Model Training

- Scikit‑learn estimators
- Configurable hyperparameters
- Trained model artifacts

---

## 📈 Model Evaluation & Registry (AWS S3)

### AWS Setup
- IAM user & access keys
- S3 bucket for model registry

```python
MODEL_BUCKET_NAME = "my-model-mlopsproj162"
MODEL_PUSHER_S3_KEY = "model-registry"
```

### Features
- Model version comparison
- Threshold‑based promotion
- Previous best model retrieval

---

## 🚀 Prediction Pipeline

- Flask‑based API
- Modular prediction flow
- `/predict` and `/training` routes
- Production‑ready serving logic

---

## 🐳 Dockerization

- Lightweight Docker image
- `.dockerignore` optimization
- Fully reproducible builds

---

## 🔁 CI/CD with GitHub Actions

### Pipeline Stages
1. Code checkout
2. Docker build
3. Push image to **Amazon ECR**
4. Deploy on **EC2 self‑hosted runner**

### GitHub Secrets
```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
```

---

## ☁️ Deployment (AWS EC2)

- Ubuntu 24.04 EC2 instance
- Docker installed
- GitHub self‑hosted runner
- Port **5000** exposed

Access App:
```
http://<EC2_PUBLIC_IP>:5000
```

---

## 🎯 Why This Project Stands Out

✔ Shows **real production ML lifecycle**  
✔ Demonstrates **cloud + DevOps + ML** integration  
✔ Emphasizes **clean architecture & scalability**  
✔ Mirrors **industry MLOps workflows**  
✔ Recruiter‑friendly & enterprise‑ready

---

## 📌 Final Note

This project is not just about training a model — it’s about **engineering an ML system that survives in production**.

If you are a recruiter or reviewer: **this repository reflects hands‑on, end‑to‑end MLOps capability.** 🚀
