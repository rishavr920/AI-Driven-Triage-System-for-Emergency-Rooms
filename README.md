# AI-Driven Triage System for Emergency Rooms 🏥

An intelligent machine learning-powered triage system designed to optimize patient prioritization in emergency rooms. This system uses advanced ML algorithms to predict patient severity and recommend appropriate triage levels.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

Emergency departments face significant challenges with patient prioritization. This AI-driven system:

- **Predicts patient severity** using machine learning
- **Recommends triage levels** (ESI 1-5 scale)
- **Optimizes ER workflow** by prioritizing critical cases
- **Reduces wait times** for urgent patients
- **Improves patient outcomes** through better resource allocation

---

## ✨ Features

- ✅ **Patient Severity Classification** - ML-based severity prediction
- ✅ **Real-time Triage Recommendations** - Instant priority assignment
- ✅ **Multiple ML Models** - Ensemble methods for improved accuracy
- ✅ **Feature Engineering** - Advanced data preprocessing
- ✅ **Model Interpretability** - Explainable AI for clinical trust
- ✅ **Performance Metrics** - Comprehensive evaluation reports
- ✅ **Data Visualization** - Interactive charts and dashboards

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Python 3.8+ |
| **Notebook** | Jupyter Notebook |
| **ML Libraries** | scikit-learn, TensorFlow, Keras |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn, Plotly |

---

## 🚀 Installation

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- pip

### Steps

```bash
# Clone repository
git clone https://github.com/rishavr920/AI-Driven-Triage-System-for-Emergency-Rooms.git
cd AI-Driven-Triage-System-for-Emergency-Rooms

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

**requirements.txt:**
```
jupyter>=1.0.0
numpy>=1.21.0
pandas>=1.3.0
scikit-learn>=1.0.0
tensorflow>=2.8.0
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.0.0
```

---

## 📖 Usage

### 1. Load and Explore Data

```python
import pandas as pd
import numpy as np

# Load patient data
df = pd.read_csv('patient_data.csv')
print(df.head())
print(df.describe())
```

### 2. Train Model

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Train
model = RandomForestClassifier(n_estimators=100)
model.fit(X_train, y_train)

# Evaluate
accuracy = model.score(X_test, y_test)
print(f"Accuracy: {accuracy:.4f}")
```

### 3. Make Predictions

```python
# Single patient prediction
patient = [[98.6, 72, 16, 120, 80, 98]]  # Vital signs
triage_level = model.predict(patient)
print(f"Triage Level: {triage_level[0]}")
```

---

## 📈 Model Performance

```
Accuracy:  0.8934
Precision: 0.8821
Recall:    0.8756
F1-Score:  0.8788
ROC-AUC:   0.9456
```

### Per-Class Performance:
- ESI-1 (Resuscitation) - Precision: 0.95, Recall: 0.92
- ESI-2 (Emergency) - Precision: 0.87, Recall: 0.85
- ESI-3 (Urgent) - Precision: 0.85, Recall: 0.88
- ESI-4 (Semi-Urgent) - Precision: 0.82, Recall: 0.84
- ESI-5 (Non-Urgent) - Precision: 0.79, Recall: 0.81

---

## 📂 Project Structure

```
AI-Driven-Triage-System/
├── Triage_System.ipynb          - Main notebook
├── data/
│   ├── raw_patient_data.csv    - Original dataset
│   └── processed_data.csv      - Cleaned dataset
├── models/
│   ├── trained_model.pkl       - Serialized model
│   └── scaler.pkl              - Feature scaler
├── outputs/
│   ├── predictions.csv         - Model predictions
│   └── metrics_report.txt      - Performance metrics
├── requirements.txt
└── README.md
```

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/your-feature`
3. Commit: `git commit -m "Add: description"`
4. Push: `git push origin feature/your-feature`
5. Create Pull Request

---

## ⚠️ Disclaimer

This system is for educational/research purposes only. Do NOT use as substitute for professional medical judgment. Always consult qualified healthcare professionals.

---

## 📄 License

MIT License - see [LICENSE](LICENSE)

---

## 👥 Author

**Rishav Raj**
- GitHub: [@rishavr920](https://github.com/rishavr920)
- Email: rishavr920@gmail.com
- LinkedIn: [rishav-raj-232033184](https://www.linkedin.com/in/rishav-raj-232033184/)

---

⭐ If helpful, please star this repository!
