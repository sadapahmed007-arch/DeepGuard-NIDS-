# 🛡️ DeepGuard NIDS – Machine Learning-Based Network Intrusion Detection System

DeepGuard NIDS is a Python-based Network Intrusion Detection System designed to monitor network traffic, identify suspicious activities, classify potential cyberattacks, and generate security alerts using Machine Learning techniques.

The project provides a security monitoring dashboard with traffic analysis, threat assessment, attack classification, and manual IP blocking recommendations.

## 📌 Project Overview

DeepGuard NIDS aims to provide an intelligent network security monitoring environment by combining Machine Learning models with a real-time traffic simulation and threat detection engine.

The system analyzes network traffic features, predicts potential attack categories, evaluates threat severity, and displays security events through an interactive dashboard.

It also supports multiple machine learning models, allowing users to compare their detection performance and select an active model.

## ✨ Key Features

### 1. Network Traffic Monitoring
- Network traffic event monitoring
- Source and destination IP tracking
- Port and protocol analysis
- Packet size monitoring
- Traffic history and logging

### 2. Machine Learning-Based Detection
- Random Forest classification
- XGBoost classification
- MLP-based neural network models
- Isolation Forest anomaly detection
- Multiple model selection
- Attack prediction and confidence scores

### 3. Attack Classification

The system includes categories for detecting and classifying:

- Denial of Service (DoS)
- Distributed Denial of Service (DDoS)
- Brute Force
- Port Scanning
- Botnet
- Web Attacks
- Infiltration
- Normal Traffic

### 4. Threat Assessment
- Threat severity evaluation
- IP-based strike tracking
- Security risk assessment
- Threat level calculation
- Suspicious IP monitoring
- Manual IP blocking recommendations

### 5. Security Alert System
- Automated attack alerts
- Severity-based notifications
- Attack source identification
- Confidence score monitoring
- Recent security event tracking

### 6. Security Dashboard
- Total traffic statistics
- Total detected attacks
- Pending security alerts
- Blocked IP statistics
- Attack type breakdown
- Protocol distribution
- Overall threat level

### 7. Model Evaluation
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Feature importance
- Model training metrics

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Backend Framework | Flask |
| Frontend | HTML5, CSS3, JavaScript |
| Database | MySQL, SQLite |
| ORM | SQLAlchemy |
| Machine Learning | Scikit-learn |
| Classification Models | Random Forest, XGBoost |
| Neural Network Models | MLPClassifier |
| Anomaly Detection | Isolation Forest |
| Data Processing | Pandas, NumPy |
| Model Serialization | Joblib |
| Dataset | KDD Cup 99 |
| API | REST API |

## 🧠 Machine Learning Models

DeepGuard NIDS includes multiple model configurations:

| Model | Purpose |
|---|---|
| Random Forest | Traffic classification |
| XGBoost | Gradient boosting-based classification |
| MLP | Neural network-based classification |
| Isolation Forest | Anomaly detection |

The training pipeline uses the KDD Cup 99 dataset for model training and evaluation.

Note: The current training script uses MLPClassifier implementations for the LSTM and 1D CNN model labels. These are not actual LSTM or CNN architectures.

## 📂 Project Structure

```text
Deepguard-NIDS/
│
├── README.md
│
└── deepguard-nids/
    │
    ├── backend/
    │   ├── api/
    │   │   └── app.py
    │   │
    │   ├── database/
    │   │   └── models.py
    │   │
    │   ├── defense/
    │   │   └── defense_engine.py
    │   │
    │   ├── realtime/
    │   │   └── detection_engine.py
    │   │
    │   ├── services/
    │   │   ├── model_loader.py
    │   │   └── train_model.py
    │   │
    │   ├── models/
    │   │   ├── rf_model.joblib
    │   │   ├── xgb_model.joblib
    │   │   ├── lstm_model.joblib
    │   │   ├── cnn_1d_model.joblib
    │   │   └── ae_model.joblib
    │   │
    │   └── data/
    │       └── real_traffic_stream.csv
    │
    ├── config/
    │   └── settings.py
    │
    ├── data/
    │   └── deepguard.db
    │
    ├── frontend/
    │   ├── index.html
    │   ├── css/
    │   │   └── styles.css
    │   └── js/
    │       └── app.js
    │
    ├── requirements.txt
    └── setup_db.py
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/DeepGuard-NIDS.git
```

### 2. Navigate to the Project Folder

```bash
cd DeepGuard-NIDS/deepguard-nids
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

For model training, install XGBoost as an additional dependency:

```bash
pip install xgboost
```

### 6. Configure the Database

The project supports MySQL and SQLite.

For SQLite on Windows Command Prompt:

```cmd
set DB_TYPE=sqlite
```

For Linux / macOS:

```bash
export DB_TYPE=sqlite
```

Alternatively, configure MySQL in `config/settings.py` and create the required database.

### 7. Run the Application

From the `deepguard-nids` directory:

```bash
python backend/api/app.py
```

### 8. Open the Dashboard

```text
http://127.0.0.1:5000
```

## 📊 Dataset and Model Training

The model training pipeline uses the KDD Cup 99 dataset.

The training process includes:

1. Dataset loading
2. Feature selection
3. Data preprocessing
4. Label encoding
5. Training and testing data splitting
6. Machine learning model training
7. Model evaluation
8. Saving trained models and evaluation metrics

To train the models:

```bash
python backend/services/train_model.py
```

The training process downloads the KDD Cup 99 dataset through Scikit-learn when required.

## 🔐 Security and Limitations

- The current traffic monitoring engine includes simulated traffic events.
- The application does not currently implement direct packet capture from a live network interface.
- IP blocking is manual and requires user action; automatic blocking is not enabled.
- Detection performance depends on the training dataset and model configuration.
- Model evaluation metrics should be interpreted using the actual training and testing process.
- This project is intended for educational and research purposes, not as a replacement for enterprise network security systems.

## 🎯 Project Objectives

- Detect suspicious network activities.
- Classify potential cyberattacks using Machine Learning.
- Monitor network traffic and security events.
- Evaluate different detection models.
- Improve network threat visibility.
- Provide an interactive security monitoring dashboard.

## 👨‍💻 Author

**Your Name**

GitHub: https://github.com/sadapahmed007-arch

## 📄 License

No license has been specified. All rights reserved unless a license is added to this repository.
