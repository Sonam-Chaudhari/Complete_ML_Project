# Complete Machine Learning Project – Student Performance Indicator

## Overview  
This project implements a complete Machine Learning pipeline to predict student performance indicators using various student data features.  
It follows **best practices and industry standards** for project structure, modular programming, logging, exception handling, and deployment, making it a scalable and maintainable ML solution.
This project is for learning purpose to understand the complete cycle of MLops and I have followed Krish naik in the learning journey.

---

## Project Highlights  
- **Standard Project Structure:** Clean separation of data, notebooks, source code, and deployment scripts.  
- **GitHub Integration:** Full version control and collaboration support using Git and GitHub.  
- **Modular Programming:** Pipeline broken down into reusable, independent components.  
- **Robust Logging & Exception Handling:** Custom logger and exception classes for better error tracking and debugging.  
- **Complete ML Workflow:** Data ingestion, cleaning, feature engineering, EDA, model training, hyperparameter tuning, evaluation, best model selection, and persistence.  
- **Local Deployment:** Flask-based API to serve the trained model for inference on localhost.  
- **CI/CD Ready:** Project structured to support continuous integration and deployment workflows.  

---

## Detailed Breakdown

### 1. Project Setup & GitHub Integration  
- Initialized Git repository for source code version control.  
- Connected the project to a remote GitHub repository for backup and collaboration.  
- Used `.gitignore` to exclude unnecessary files (e.g., datasets, virtual environments).  
- Committed code in logical chunks with clear commit messages to maintain history and track progress.

---

### 2. Modular Programming Approach  
The codebase is organized into independent modules, enabling easy maintenance and scalability:  
- **Data Ingestion:** Responsible for loading raw data from files or sources.  
- **Data Transformation:** Handling missing values, categorical encoding, scaling, and feature engineering.  
- **Model Training:** Training various ML models with clean APIs.  
- **Model Evaluation:** Evaluating models using standard metrics and selecting the best one.  
- **Prediction Pipeline:** Loading the best model and making predictions on new data.  

Each component is placed in a dedicated folder inside `src/components`, following separation of concerns.

---

### 3. Logging & Exception Handling  
- Created a **custom logger** (`logger.py`) to track execution flow and capture runtime information with timestamps and log levels (INFO, ERROR, DEBUG).  
- Defined **custom exceptions** (`exception.py`) to provide meaningful error messages, improving debugging efficiency.  
- Integrated logging and exception handling throughout the pipeline to catch and log unexpected failures gracefully without abrupt termination.

---

### 4. Environment Setup (`requirements.txt` & `setup.py`)  
- Listed all required dependencies in `requirements.txt` for easy environment replication via `pip install -r requirements.txt`.  
- Created `setup.py` to package the source code, allowing easy installation and deployment if needed.  
- Virtual environments recommended to maintain isolated Python environments.

---

### 5. Data Cleaning & Preprocessing  
- Loaded dataset from CSV files stored in the `data/` directory.  
- Performed data cleaning: handled missing values, removed duplicates, and ensured consistent data types.  
- Applied categorical encoding (e.g., One-Hot, Label Encoding) for categorical variables.  
- Scaled numerical features using StandardScaler or MinMaxScaler to improve model convergence.

---

### 6. Exploratory Data Analysis (EDA)  
- Created Jupyter notebooks in the `notebooks/` folder to explore the dataset visually and statistically.  
- Plotted distributions, correlation heatmaps, box plots, and scatter plots to understand relationships and detect outliers.  
- Identified key features impacting student performance.  
- Documented insights that informed feature selection and engineering decisions.

---

### 7. Model Training & Hyperparameter Tuning  
- Trained multiple regression models such as Linear Regression, Decision Tree Regressor, and Random Forest Regressor.  
- Implemented hyperparameter tuning using `GridSearchCV` to optimize model parameters systematically.  
- Trained pipelines encapsulating preprocessing steps + model training for cleaner workflow and easier reproducibility.  
- Saved trained models using `pickle` or `joblib` for future inference.

---

### 8. Model Evaluation & Best Model Selection  
- Evaluated models on training and test sets using metrics like R² score, Mean Absolute Error (MAE), and Mean Squared Error (MSE).  
- Compared model performances and selected the best-performing model based on generalization ability and accuracy.  
- Logged evaluation results and generated performance reports for documentation.

---

### 9. Complete Pipeline Automation  
- Built end-to-end training and prediction pipelines that automate the entire ML workflow from raw data ingestion to final prediction.  
- Pipelines handle all intermediate steps without manual intervention, improving efficiency and reproducibility.  
- Modular pipelines allow easy extension or swapping of components as required.

---

### 10. Local Deployment with Flask  
- Developed a simple Flask API (`app.py`) to serve the best model locally.  
- API accepts input features via HTTP requests and returns prediction results in JSON format.  
- Demonstrates ability to deploy ML models for real-time inference on local or production environments.

---

### 11. CI/CD Ready Structure  
- Project structured to facilitate automated testing, integration, and deployment using CI/CD pipelines (e.g., GitHub Actions, Jenkins).  
- Clear separation of source code, dependencies, tests (can be added), and deployment scripts supports scalable development workflows.  
- Ready for future extension to cloud deployment or containerization with Docker.

---


