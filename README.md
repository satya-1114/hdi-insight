# 🌍 HDI Insight

### A Comprehensive Measure of Well-Being

<p align="center">
  <b>An intelligent machine learning platform for predicting and analyzing the Human Development Index (HDI) using key socioeconomic indicators.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12+-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Flask-REST_API-black?logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Vite-Frontend-646CFF?logo=vite&logoColor=white" alt="Vite">
  <img src="https://img.shields.io/badge/Status-Completed-success" alt="Status">
</p>

---

## 📖 Overview

**HDI Insight** is a full-stack machine learning application designed to predict a country's **Human Development Index (HDI)** using important socioeconomic indicators.

Traditional measures of development often focus primarily on economic growth. However, human well-being depends on multiple dimensions, including:

- 🏥 Health and longevity
- 🎓 Access to education
- 💰 Standard of living

HDI Insight combines these dimensions through machine learning to estimate a country's HDI score and classify its level of human development.

The platform uses a **Linear Regression** model trained on human development data and provides predictions through a **Flask REST API** connected to a modern **React frontend**.

The project demonstrates a complete machine learning workflow:

> **Data Collection → Data Preprocessing → Feature Selection → Model Training → Model Evaluation → REST API Integration → Frontend Visualization**

---

## 🎯 Project Objective

The primary objective of this project is to build an intelligent and accessible platform capable of estimating human development using measurable socioeconomic indicators.

The project aims to:

- Predict the Human Development Index of a country.
- Analyze the relationship between health, education, income, and human development.
- Classify predicted HDI scores into standard development categories.
- Provide an interactive interface for entering socioeconomic indicators.
- Visualize predictions and model performance.
- Demonstrate an end-to-end machine learning application.
- Provide transparent information about the model and its evaluation metrics.

---

## 💡 Problem Statement

Economic indicators alone do not provide a complete picture of people's quality of life.

A country may experience economic growth while still facing challenges related to:

- Life expectancy
- Education
- Income distribution
- Access to opportunities

The **Human Development Index (HDI)** provides a broader perspective by combining major dimensions of human development.

HDI Insight uses machine learning to estimate HDI from key socioeconomic indicators, providing an interactive platform for exploring the relationship between these indicators and overall human development.

---

## ✨ Key Features

### 🤖 Machine Learning-Based HDI Prediction

Predicts a country's HDI score using a trained regression model.

### 🌎 Country-Level Analysis

Users can enter socioeconomic indicators for a country and receive an estimated HDI score.

### 🏷️ Human Development Classification

Automatically classifies predictions into:

- Low Human Development
- Medium Human Development
- High Human Development
- Very High Human Development

### 📊 Analytics Dashboard

Provides visual summaries of predictions and human development data.

### 📈 Model Performance Metrics

Displays important machine learning evaluation metrics such as:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

### 🔍 Model Transparency

Provides information about:

- The machine learning algorithm
- Input features
- Model evaluation
- Prediction methodology

### ⚡ REST API

A Flask-based backend provides structured JSON APIs for prediction and model information.

### 💻 Modern Web Interface

A responsive React frontend provides a clean research-oriented user experience.

---

## 🧠 How the Prediction Works

The model predicts HDI using four major socioeconomic indicators:

| Feature | Description |
|---|---|
| **Life Expectancy** | Average number of years a person is expected to live |
| **Expected Years of Schooling** | Number of years of education a child is expected to receive |
| **Mean Years of Schooling** | Average number of completed years of education |
| **GNI per Capita** | Gross National Income per person |

The trained model processes these values and generates a predicted HDI score.

### Prediction Flow

```text
User Enters Socioeconomic Indicators
                │
                ▼
       React Prediction Form
                │
                ▼
        Axios HTTP Request
                │
                ▼
          Flask REST API
                │
                ▼
        Input Validation Layer
                │
                ▼
     Trained Linear Regression Model
                │
                ▼
          Predicted HDI Score
                │
                ▼
      HDI Category Classification
                │
                ▼
       JSON Response to Frontend
                │
                ▼
      Dashboard & Result Display
```

---

## 🏷️ HDI Classification

The predicted HDI score is classified into a human development category.

| HDI Score | Human Development Category |
|---|---|
| `0.800 and above` | 🟢 Very High |
| `0.700 – 0.799` | 🔵 High |
| `0.550 – 0.699` | 🟡 Medium |
| `Below 0.550` | 🔴 Low |

### Classification Logic

```python
def classify_hdi(score):
    if score >= 0.8:
        return "Very High"
    elif score >= 0.7:
        return "High"
    elif score >= 0.55:
        return "Medium"
    else:
        return "Low"
```

---

# 🏗️ System Architecture

HDI Insight follows a modular three-tier architecture consisting of:

1. **Frontend Layer**
2. **Backend/API Layer**
3. **Machine Learning Layer**

```text
┌──────────────────────────────┐
│       React Frontend         │
│                              │
│  • Home                      │
│  • Prediction                │
│  • Dashboard                 │
│  • Analytics                 │
│  • Model Information         │
└──────────────┬───────────────┘
               │
               │ HTTP / JSON
               ▼
┌──────────────────────────────┐
│       Flask REST API         │
│                              │
│  • Request Handling          │
│  • Input Validation          │
│  • Prediction Endpoint       │
│  • Model Information         │
│  • Error Handling            │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│    Machine Learning Layer    │
│                              │
│  • Data Preprocessing        │
│  • Feature Selection         │
│  • Linear Regression         │
│  • HDI Prediction            │
│  • Category Classification   │
└──────────────────────────────┘
```

### Overall Architecture Flow

```text
React Frontend
      ↓
Flask REST API
      ↓
Prediction Service
      ↓
Serialized Scikit-learn Model
      ↓
HDI Prediction
      ↓
Development Category
      ↓
JSON Response
      ↓
Dashboard & Analytics
```

---

# 🛠️ Technology Stack

## Frontend

| Technology | Purpose |
|---|---|
| **React** | User interface development |
| **Vite** | Fast development and production builds |
| **JavaScript** | Frontend application logic |
| **Axios** | Communication with the Flask API |
| **Tailwind CSS** | UI styling |
| **Recharts** | Data visualization and charts |

## Backend

| Technology | Purpose |
|---|---|
| **Python** | Backend and machine learning development |
| **Flask** | REST API development |
| **Flask-CORS** | Cross-origin frontend/backend communication |

## Machine Learning & Data Science

| Technology | Purpose |
|---|---|
| **Scikit-learn** | Model training and evaluation |
| **Pandas** | Data manipulation and preprocessing |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |
| **Seaborn** | Exploratory data visualization |
| **Pickle** | Model serialization |

## Data Source

| Technology | Purpose |
|---|---|
| **Kaggle** | Human development dataset source |
| **KaggleHub** | Programmatic dataset retrieval |

## Development Tools

- Git
- GitHub
- Visual Studio Code
- npm
- pip
- Python Virtual Environment

---

# 📊 Machine Learning Workflow

The machine learning pipeline follows a structured development process.

## 1. Dataset Acquisition

The Human Development dataset is retrieved programmatically using KaggleHub.

```python
import kagglehub

path = kagglehub.dataset_download(
    "undp/human-development-index"
)

print("Dataset downloaded to:", path)
```

---

## 2. Data Exploration

The dataset is loaded into a Pandas DataFrame and analyzed for:

- Column names
- Data types
- Missing values
- Duplicate records
- Feature ranges
- Statistical distributions

---

## 3. Data Cleaning

The preprocessing stage includes:

- Handling missing values
- Removing duplicate records
- Standardizing column names
- Correcting inconsistent formats
- Validating numerical data

---

## 4. Feature Selection

The following features are selected as predictors:

```text
Life Expectancy
Expected Years of Schooling
Mean Years of Schooling
GNI per Capita
```

The prediction target is:

```text
Human Development Index (HDI)
```

---

## 5. Train-Test Split

The cleaned dataset is divided into:

- **80% Training Data**
- **20% Testing Data**

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

---

## 6. Model Training

The project uses Scikit-learn's **Linear Regression** algorithm.

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
```

Linear Regression was selected because it provides:

- High interpretability
- Fast training
- Fast prediction
- A transparent baseline
- Easy integration with a REST API

---

## 7. Model Evaluation

The trained model is evaluated using:

### R² Score

Measures how much of the variation in HDI is explained by the model.

### Mean Absolute Error — MAE

Measures the average absolute difference between actual and predicted HDI values.

### Root Mean Squared Error — RMSE

Measures prediction error while giving greater weight to larger errors.

```python
from sklearn.metrics import (
    r2_score,
    mean_absolute_error,
    mean_squared_error
)

predictions = model.predict(X_test)

r2 = r2_score(y_test, predictions)
mae = mean_absolute_error(y_test, predictions)
rmse = mean_squared_error(
    y_test,
    predictions,
    squared=False
)
```

> **Note:** The actual model evaluation values should be generated from the final trained model rather than manually hard-coded.

---

## 8. Model Serialization

The trained model is saved using Pickle.

```python
import pickle

with open("hdi_model.pkl", "wb") as file:
    pickle.dump(model, file)
```

This allows the Flask application to load the trained model without retraining it every time the server starts.

---

# 📂 Project Structure

```text
hdi-insight/
│
├── backend/
│   │
│   ├── app.py
│   ├── train_model.py
│   ├── requirements.txt
│   │
│   ├── model/
│   │   └── hdi_model.pkl
│   │
│   └── data/
│       └── README.md
│
├── frontend/
│   │
│   ├── public/
│   │
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── PredictionForm.jsx
│   │   │   ├── ResultCard.jsx
│   │   │   └── MetricsSummary.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Prediction.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Analytics.jsx
│   │   │   ├── ModelInfo.jsx
│   │   │   ├── About.jsx
│   │   │   └── Contact.jsx
│   │   │
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
├── docs/
│   └── HDI_Insight_Project_Documentation.pdf
│
├── .gitignore
├── LICENSE
└── README.md
```

> The exact folder structure may vary depending on the final implementation.

---

# 🚀 Getting Started

## Prerequisites

Before running the project, make sure you have installed:

- Python 3.12 or later
- Node.js 22 LTS
- npm
- Git

---

# 📥 Installation

## 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

Move into the project directory:

```bash
cd hdi-insight
```

---

# ⚙️ Backend Setup

## 2. Navigate to the Backend

```bash
cd backend
```

## 3. Create a Virtual Environment

```bash
python -m venv .venv
```

## 4. Activate the Virtual Environment

### Windows PowerShell

```powershell
.venv\Scripts\Activate.ps1
```

### Windows Command Prompt

```cmd
.venv\Scripts\activate
```

### Linux / macOS

```bash
source .venv/bin/activate
```

---

## 5. Install Backend Dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` has not yet been generated:

```bash
pip install flask flask-cors pandas numpy scikit-learn matplotlib seaborn kagglehub
```

Then generate it:

```bash
pip freeze > requirements.txt
```

---

## 6. Train the Model

If the serialized model is not already available:

```bash
python train_model.py
```

This process will:

1. Load the dataset
2. Clean the data
3. Select model features
4. Split the data
5. Train the Linear Regression model
6. Evaluate the model
7. Save the trained model

---

## 7. Start the Flask Backend

```bash
python app.py
```

The backend should run at:

```text
http://127.0.0.1:5000
```

---

# 💻 Frontend Setup

Open a new terminal.

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the Vite development server:

```bash
npm run dev
```

Open the local URL displayed in the terminal.

Typically:

```text
http://localhost:5173
```

---

# 🔌 API Documentation

## 1. Health Check

### Endpoint

```http
GET /
```

### Example Response

```json
{
    "status": "HDI Insight API is running"
}
```

---

## 2. Predict HDI

### Endpoint

```http
POST /predict
```

### Request Body

```json
{
    "country": "Example Country",
    "life_expectancy": 75,
    "expected_schooling": 15,
    "mean_schooling": 10,
    "gni_per_capita": 25000
}
```

### Example Response

```json
{
    "success": true,
    "predicted_hdi": 0.782,
    "category": "High",
    "country": "Example Country"
}
```

---

## 3. Model Information

### Endpoint

```http
GET /model-info
```

### Example Response

```json
{
    "model": "Linear Regression",
    "r2_score": "<actual-model-value>",
    "mae": "<actual-model-value>",
    "rmse": "<actual-model-value>"
}
```

---

# 🖥️ Application Pages

## 🏠 Home Page

The Home page introduces the HDI Insight platform and explains its purpose.

Main elements include:

- Project introduction
- Human development overview
- Call-to-action buttons
- Navigation to prediction and analytics

---

## 🔮 Prediction Page

The Prediction page allows users to enter:

- Country name
- Life expectancy
- Expected years of schooling
- Mean years of schooling
- GNI per capita

After submitting the form, the application displays:

- Predicted HDI score
- Human development category
- Country information
- Interpretive result summary

---

## 📊 Dashboard Page

The Dashboard displays summary information such as:

- Predicted HDI
- Human Development Category
- Country
- Prediction Date
- Model Performance

---

## 📈 Analytics Page

The Analytics page provides visual comparisons of predictions and human development data.

Charts can be used to compare:

- HDI values
- Countries
- Prediction results
- Human development categories

---

## 🧠 Model Information Page

The Model Information page improves transparency by displaying:

- Machine learning algorithm
- Input features
- Model evaluation metrics
- Prediction methodology

---

## ℹ️ About Page

The About page explains:

- Project motivation
- Project objectives
- Importance of measuring human development
- Intended users of the platform

---

## 📬 Contact Page

The Contact page provides an interface for:

- Feedback
- Questions
- Collaboration inquiries

---

# 🎨 Design System

The frontend uses a restrained, research-oriented visual identity.

| Element | Color | Purpose |
|---|---|---|
| Primary Background | `#F5F1E8` | Main application background |
| Cards | `#FFFFFF` | Cards, tables, and dialogs |
| Primary Text | `#18181B` | Headings and body text |
| Secondary Text | `#52525B` | Labels and descriptions |
| Primary Accent | `#3F5C3A` | Buttons, links, active states |
| Hover | `#31472D` | Interactive hover states |
| Border | `#E7DED1` | Dividers and outlines |

The interface is designed to resemble a professional research and analytics platform rather than a conventional student dashboard.

---

# 🧪 Testing

The application should be tested using:

### Valid Inputs

Test realistic values for:

- Life expectancy
- Education indicators
- GNI per capita

### Invalid Inputs

Test:

- Missing fields
- Empty values
- Non-numeric input
- Negative values
- Extremely large values
- Invalid request payloads

### Integration Testing

Verify that:

```text
Frontend Form
     ↓
Flask API
     ↓
ML Model
     ↓
Prediction
     ↓
JSON Response
     ↓
Frontend Result
```

works correctly from end to end.

---

# 🔐 Security Considerations

Sensitive information should never be committed to the repository.

Do not upload:

```text
.env
kaggle.json
API keys
Passwords
Access tokens
Virtual environments
node_modules
```

Example `.gitignore`:

```gitignore
# Python
__pycache__/
*.py[cod]
.venv/
venv/

# Machine Learning / Local Data
*.pkl
data/

# Environment Variables
.env
.env.*

# Kaggle Credentials
kaggle.json

# Node.js
node_modules/
dist/

# IDE
.vscode/
.idea/

# Operating System
.DS_Store
Thumbs.db
```

> If your application requires the trained `.pkl` model to run directly after cloning, remove `*.pkl` from `.gitignore` and commit only the intended model artifact.

---

# 🚀 Deployment

## Local Deployment

Start the Flask backend:

```bash
cd backend
python app.py
```

Start the React frontend:

```bash
cd frontend
npm run dev
```

---

## Production Deployment

For production deployment:

- Build the React frontend.
- Configure environment variables.
- Disable Flask debug mode.
- Configure CORS for trusted origins.
- Use HTTPS.
- Use a production-ready server for the Flask application.
- Deploy the frontend and backend to suitable hosting platforms.

Build the React frontend with:

```bash
npm run build
```

---

# 👥 Intended Users

HDI Insight can be useful for:

- 🎓 Students
- 👨‍🏫 Educators
- 🔬 Researchers
- 📊 Data analysts
- 🏛️ Policy researchers
- 💻 Machine learning learners

---

# 📌 Use Cases

### Research and Analysis

A researcher can enter socioeconomic indicators and estimate the corresponding HDI level.

### Education

A lecturer can demonstrate how machine learning can model relationships between socioeconomic indicators and human development.

### Machine Learning Demonstration

Students can explore a complete ML pipeline from dataset acquisition to deployment.

### Portfolio Project

The project demonstrates practical experience with:

- Data preprocessing
- Regression
- Model evaluation
- REST APIs
- Full-stack development
- Frontend visualization

---

# 🔮 Future Scope

The project can be extended with several improvements.

### 🤖 Advanced Machine Learning Models

Compare Linear Regression with:

- Random Forest Regressor
- Gradient Boosting
- XGBoost
- Other regression models

### 🗄️ Database Integration

Add a persistent database to store:

- Users
- Countries
- Predictions
- Prediction history

### 🔐 User Authentication

Allow users to:

- Create accounts
- Sign in securely
- Save predictions
- Revisit previous analyses

### 📈 Historical Trend Analysis

Support analysis of HDI changes across multiple years.

### 🔮 Time-Series Forecasting

Predict future HDI trends based on historical data.

### 🌍 Expanded Dataset

Include additional socioeconomic indicators and more historical records.

### ☁️ Cloud Deployment

Deploy the application using production-grade cloud infrastructure.

---

# 📄 Project Documentation

Complete project documentation is available in:

```text
docs/HDI_Insight_Project_Documentation.pdf
```

The documentation includes:

- Project Description
- Use-Case Scenarios
- Technical Architecture
- Prerequisites
- Project Workflow
- Model Selection
- Dataset Acquisition
- Machine Learning Pipeline
- Flask Backend Development
- React Frontend Development
- Design System
- Deployment
- Application Pages
- Conclusion
- Future Scope

---

# ⚠️ Disclaimer

This project is developed for **educational, research, and demonstration purposes**.

The HDI values generated by this application are **machine learning predictions** and should not be interpreted as official Human Development Index values.

Official HDI values should be obtained from authoritative international development data sources.

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

To contribute:

1. Fork the repository.
2. Create a new branch.

```bash
git checkout -b feature/your-feature-name
```

3. Make your changes.
4. Commit your changes.

```bash
git commit -m "Add new feature"
```

5. Push the branch.

```bash
git push origin feature/your-feature-name
```

6. Open a Pull Request.

---

# 📜 License

This project is intended primarily for educational and academic purposes.

If a license file is included in the repository, usage and distribution are governed by the terms of that license.

---

# 👨‍💻 Author

## Annamneedi Satyanarayana

**B.Tech — Computer Science and Engineering**

GitHub: `satya-1114`

---

<p align="center">
  <b>HDI Insight — Using Data and Machine Learning to Better Understand Human Development</b>
</p>

<p align="center">
  ⭐ If you find this project useful, consider giving the repository a star.
</p>
