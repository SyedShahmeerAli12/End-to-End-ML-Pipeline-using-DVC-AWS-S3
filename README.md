#  Ham Spam Classifier: End-to-End Machine Learning Pipeline with DVC and AWS S3

Welcome to the **Ham Spam Classifier** project! This is a sample project demonstrating how to build an **end-to-end machine learning pipeline** for classifying emails as **Ham** or **Spam**. The project leverages **DVC (Data Version Control)** for managing data and model versions, and **AWS S3** for storing datasets and model artifacts.

---



##  Project Overview

The goal of this project is to build a **Ham Spam Classifier** that can accurately classify emails as either **Ham** (legitimate) or **Spam** (unwanted). The project follows an **end-to-end machine learning pipeline**, including:

- **Data Preprocessing**: Cleaning and preparing the dataset.
- **Model Training**: Training a machine learning model (e.g., Logistic Regression, Random Forest).
- **Model Evaluation**: Evaluating the model's performance using metrics like accuracy, precision, recall, and F1-score.
- **Model Versioning**: Using **DVC** to version control datasets, models, and metrics.
- **Storage**: Storing datasets and model artifacts in **AWS S3**.

---

##  Tech Stack

- **Programming Language**: Python
- **Machine Learning Framework**: Scikit-learn
- **Data Version Control**: DVC
- **Cloud Storage**: AWS S3
- **Logging**: Python's `logging` module
- **Environment Management**: `pip` and `requirements.txt`

---


---

##  How It Works

1. **Data Preprocessing**:
   - The raw dataset (emails) is cleaned and preprocessed.
   - Text data is tokenized, stopwords are removed, and features are extracted.

2. **Model Training**:
   - A machine learning model (e.g., Logistic Regression) is trained on the preprocessed data.
   - The trained model is saved to the `models/` directory.

3. **Model Evaluation**:
   - The model's performance is evaluated using metrics like accuracy, precision, recall, and F1-score.
   - Metrics are saved to the `metrics/` directory.

4. **DVC Integration**:
   - DVC is used to version control datasets, models, and metrics.
   - Changes are tracked using `dvc add` and `dvc push`.

5. **AWS S3 Integration**:
   - Datasets and model artifacts are stored in an **AWS S3 bucket**.
   - DVC is configured to use the S3 bucket as remote storage.

---

## Setup and Installation

### Prerequisites
- Python 3.8+
- AWS CLI configured with access to an S3 bucket.
- DVC installed (`pip install dvc`).

### Steps


   1. Clone the repository:
   ```bash
   git clone https://github.com/SyedShahmeerAli12/End-to-End-ML-Pipeline-using-DVC-AWS-S3.git
   ```


   2. Install Dependencies:
:
   ```bash
  pip install -r requirements.txt
   ```

   3. Configure DVC with AWS S3:
   ```bash
    dvc remote add -d dvcstore s3://your-s3-bucket-name
   ```

   4. Pull Data and Models from DVC:

   ```bash
dvc pull  
 ```