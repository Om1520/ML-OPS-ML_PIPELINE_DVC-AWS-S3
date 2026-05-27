# 🚀 End-to-End MLOps Pipeline with DVC, DVCLive & AWS S3

![Python](https://img.shields.io/badge/Python-3.x-blue)
![DVC](https://img.shields.io/badge/DVC-Data%20Version%20Control-purple)
![AWS S3](https://img.shields.io/badge/AWS-S3-orange)
![DVCLive](https://img.shields.io/badge/DVCLive-Experiment%20Tracking-green)
![MLOps](https://img.shields.io/badge/MLOps-Pipeline-red)

A production-ready **Machine Learning workflow**, built using **DVC, DVCLive, and AWS S3**, demonstrating how to move from experimentation to a scalable and reproducible MLOps system.

This project follows a structured workflow for:

- Modular component development
- Automated pipeline execution
- Experiment tracking
- Dataset versioning
- Cloud artifact management

---

## 📌 Project Overview

The goal of this project is to build a reproducible ML system by:

- Separating **code from data**
- Creating a **modular architecture**
- Automating workflow execution using **DVC**
- Tracking experiments using **DVCLive**
- Storing datasets and artifacts using **AWS S3**

This approach ensures:

✅ Reproducibility  
✅ Experiment Tracking  
✅ Scalable Data Management  
✅ Automated Workflow Execution  

---

# 🛠️ Tech Stack

| Category | Technology |
|------------|------------|
| Language | Python |
| Version Control | Git |
| Data Versioning | DVC |
| Cloud Storage | AWS S3 |
| Experiment Tracking | DVCLive |
| Pipeline Orchestration | DVC Pipelines |
| Configuration Management | YAML |
| ML Framework | Scikit-learn |

---

# 🏗️ Workflow Architecture

```text
GitHub Repository
        ↓
Local Development
        ↓
Experimentation
        ↓
Modular Source Components
        ↓
DVC Pipeline Automation
        ↓
Centralized Parameters
        ↓
DVCLive Experiment Tracking
        ↓
AWS S3 Remote Storage
        ↓
Versioned Production ML Workflow
```

---

# 📂 Project Structure

```text
├── experiments/
│
├── src/
│   ├── data_ingestion.py
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── model_training.py
│   ├── model_evaluation.py
│   ├── logger.py
│   └── exception.py
│
├── data/
│   ├── raw/
│   ├── processed/
│
├── artifacts/
│
├── dvc.yaml
├── params.yaml
├── requirements.txt
├── setup.py
├── README.md
└── .gitignore
```

---

# ⚙️ Core Workflow Components

## 1️⃣ Experimentation Phase

Responsible for:

- Rapid prototyping
- Testing ideas
- Building isolated components
- Initial implementation validation

Development flow:

```text
Experimentation
        ↓
Component Development
        ↓
Module Integration
        ↓
Pipeline Automation
```

---

## 2️⃣ Modular Component Development

The project follows a modular design where each component is built independently.

Includes:

- Data ingestion
- Data preprocessing
- Feature engineering
- Model training
- Model evaluation

Benefits:

✔ Reusable code  

✔ Easier debugging  

✔ Better scalability  

---

## 3️⃣ Parameterized Configuration

All hyperparameters and settings are managed centrally.

Configuration file:

```yaml
params.yaml
```

Example:

```yaml
test_size: 0.2

n_estimators: 100

max_features: sqrt
```

Advantages:

✔ No hardcoded values

✔ Faster experimentation

✔ Better reproducibility

✔ Easier tuning

---

## 4️⃣ DVC Pipeline Automation

The workflow is managed using:

```yaml
dvc.yaml
```

Benefits:

- Dependency tracking
- Automatic stage execution
- Reproducibility
- Parameter management

Initialize DVC:

```bash
dvc init
```

Run workflow:

```bash
dvc repro
```

Visualize pipeline:

```bash
dvc dag
```

---

## 5️⃣ Experiment Tracking with DVCLive

DVCLive tracks experiment details without affecting Git history.

Track:

- Metrics
- Parameters
- Logs
- Performance plots

Run experiment:

```bash
dvc exp run
```

Compare experiments:

```bash
dvc exp show
```

Apply experiment:

```bash
dvc exp apply experiment-name
```

Remove experiment:

```bash
dvc exp remove experiment-name
```

Features:

✔ Metrics tracking  

✔ Parameter tracking  

✔ Experiment comparison  

✔ Easy rollback  

---

# ☁️ AWS S3 Integration

Large datasets and model artifacts are excluded from Git and stored remotely.

Install dependencies:

```bash
pip install dvc[s3]

pip install awscli
```

Configure AWS:

```bash
aws configure
```

Add DVC remote:

```bash
dvc remote add -d dvcstore s3://your-bucket-name
```

Push artifacts:

```bash
dvc commit

dvc push
```

Pull artifacts:

```bash
dvc pull
```

Benefits:

✔ Lightweight repositories

✔ Cloud-backed storage

✔ Team collaboration

✔ Dataset versioning

---

# 🚀 Setup & Installation

## Clone repository

```bash
git clone https://github.com/your-username/repository-name.git

cd repository-name
```

---

## Create virtual environment

### Linux/Mac

```bash
python -m venv venv

source venv/bin/activate
```

### Windows

```bash
venv\Scripts\activate
```

---

## Install dependencies

```bash
pip install -r requirements.txt
```

---

## Initialize DVC

```bash
dvc init
```

---

## Pull data from remote storage

```bash
dvc pull
```

---

## Execute pipeline

```bash
dvc repro
```

---

# 📊 Key DVC Commands

| Command | Purpose |
|-----------|----------|
| `dvc init` | Initialize DVC |
| `dvc repro` | Run pipeline |
| `dvc dag` | Visualize dependency graph |
| `dvc exp run` | Run experiment |
| `dvc exp show` | Compare experiments |
| `dvc exp apply` | Restore experiment |
| `dvc push` | Upload data/models |
| `dvc pull` | Download data/models |

---

# 🎯 Key Learnings

Through this project:

- Built modular ML workflows
- Automated execution pipelines
- Centralized configuration management
- Tracked experiments efficiently
- Managed cloud artifacts
- Applied production-grade MLOps practices

---

# 🤝 Contributing

Contributions and suggestions are welcome.

1. Fork repository
2. Create feature branch
3. Commit changes
4. Push branch
5. Open Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

⭐ If you found this useful, consider giving the repository a star.