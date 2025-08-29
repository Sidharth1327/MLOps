# MLOps

### [1: Introduction](https://github.com/Sidharth1327/MLOps/tree/main/01-intro)

- 🔎 Overview of **MLOps** and why it matters  
- 📊 Explanation of the **MLOps Maturity Model** 
- 🚖 Introduction to the **NYC Taxi dataset** (our running example)  
- ⏱️ Hands-on notebook: calculating **trip durations** and exploring dataset basics  

### [2: Experiment Tracking](https://github.com/Sidharth1327/MLOps/tree/main/02-experiment-tracking)

Implemented ML experiment tracking workflows with **MLflow**.  
- Set up runs to capture parameters, metrics, artifacts, and source metadata.  
- Logged models both as artifacts and with framework-specific loggers.  
- Compared manual tracking (spreadsheets) vs. automated pipelines.  
- Positioned experiment tracking within the broader ML lifecycle (data → training → versioning → deployment).  
- Built a foundation for reproducibility, collaboration, and scaling experiments.  

### [3: Workflow Orchestration]
Converted a Python notebook into a streamlined Python script and built a fully operational ML pipeline.

- Optimized code by including only the essential steps required for training, validation, and model logging.
- Explored leading workflow orchestration tools (Airflow, Prefect, Dagster, Kestra, Mage) to understand their features, architecture, and application for ML pipelines.
- Implemented stepwise orchestration:
  1. **Running the Tool**: Configured the chosen tool locally and executed the simplest "hello world" workflow.
  2. **Orchestrating the Workflow**: Integrated the previous ML pipeline code to automate sequential steps in the pipeline.
  3. **Parametrizing the Workflow**: Scheduled workflows for monthly execution, dynamically selecting training data (two months prior) and validation data (one month prior).
  4. **Backfilling**: Enabled execution of workflows for historical data to ensure consistency and completeness.
  5. **Deployment (optional)**: Gained exposure to cloud deployment options for orchestrated pipelines.

- Positioned workflow orchestration as a critical step in productionizing ML pipelines for reproducibility, scalability, and maintainability.
- Built a foundation for end-to-end ML operations, integrating preprocessing, training, evaluation, and logging into a single automated flow.

