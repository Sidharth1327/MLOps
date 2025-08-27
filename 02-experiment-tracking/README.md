# 📂 Module 2: Experiment Tracking

Experimentation is at the **core of machine learning workflows**. Every time we train a model, we make decisions about data preprocessing, model architecture, hyperparameters, and evaluation metrics. Keeping track of these experiments in an organized, reproducible way is what makes the difference between a research prototype and a production-ready ML system.

---

## 🔑 Core Concepts

- **ML Experiment** → The overall process of building and validating a model.  
- **Run / Trial** → A single execution of an experiment with a specific configuration.  
- **Artifacts** → Any files produced during a run (e.g., trained models, plots, logs).  
- **Metadata** → Contextual details about the experiment (code version, environment, author, timestamp).  

Together, these elements form the **digital footprint of an ML workflow**.

---

## ❓ What is Experiment Tracking?

**Experiment tracking** is the practice of recording and organizing all relevant information associated with ML experiments, including:

- 🧑‍💻 **Source code** & versioning (Git commits, script versions)  
- 🌍 **Environment** (Python packages, Docker images, hardware configs)  
- 📊 **Data** (datasets, versions, preprocessing steps)  
- 🤖 **Model** (architecture, framework, version)  
- ⚙️ **Hyperparameters** (learning rate, batch size, optimizer)  
- 📈 **Metrics** (accuracy, loss, F1, latency, etc.)  
- 📦 **Artifacts** (models, plots, checkpoints, logs)  

Without structured tracking, reproducing results or comparing models becomes nearly impossible.

---

## ⚠️ Why is it Important?

Experiment tracking matters because it enables:

1. **Reproducibility** 🧪  
   - Anyone (including future you) can re-run an experiment with the same conditions.  

2. **Organization** 🗂️  
   - No more digging through random folders or spreadsheets to find which model performed best.  

3. **Optimization** 🚀  
   - Compare results across runs to identify the optimal hyperparameters, models, and pipelines.  

---

## ❌ Why Not Spreadsheets?

Some teams start by logging experiment details manually in Excel/Google Sheets. While this works for a few experiments, it quickly breaks down:

- Error-prone and inconsistent  
- No standard format  
- Poor visibility and collaboration  
- Cannot scale with dozens or hundreds of runs  

This is where **MLflow** comes in.  

---

## ⚡ MLflow: A Practical Tool

**MLflow** is an **open-source platform for the ML lifecycle**.  
It provides four main modules:

1. **Tracking** – Record parameters, metrics, artifacts, and metadata.  
2. **Models** – Package models for reproducible deployment across frameworks.  
3. **Model Registry** – Manage versions of models in staging, production, or archived states.  
4. **Projects** – Standardize reproducible ML projects with defined environments.  

In this module, we focus on the **Tracking API**.

---

## 📝 Tracking with MLflow

The **MLflow Tracking module** allows you to organize experiments into *runs*, logging both structured information and automatically captured metadata.

### What you can log:
- Parameters (`learning_rate=0.01`, `batch_size=64`)  
- Metrics (`accuracy=0.92`, `loss=0.15`)  
- Artifacts (trained model, confusion matrix, plots)  
- Models (serialized objects for reuse or deployment)  

### What MLflow logs automatically:
- Source code reference (Git commit, file)  
- Start and end time of each run  
- Environment details  
- Author / executor  

---

## ⚙️ Logging Models in MLflow

Two common approaches:

```python
# 1. Log model as an artifact
mlflow.log_artifact("mymodel.pkl", artifact_path="models/")

# 2. Log model with framework-specific helper
mlflow.sklearn.log_model(model, artifact_path="models/")
