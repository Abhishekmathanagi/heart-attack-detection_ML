# ❤️ Heart Disease Prediction Using Machine Learning

An interactive machine learning web application built using **Python, Scikit-learn, Pandas, and Streamlit** to predict the likelihood of heart disease based on user-provided health attributes.

The application integrates a trained **K-Nearest Neighbors (KNN)** classification model with a preprocessing pipeline to generate predictions through a simple, user-friendly interface.

> **Disclaimer:** This project is intended for educational purposes only. Its predictions are not medical diagnoses and should not be used to make healthcare decisions.

---

## 📌 Project Overview

Machine learning classification algorithms can identify patterns in datasets and use them to make predictions.

This project demonstrates how a trained machine learning model can be integrated into a web application, allowing users to enter health-related information and receive a model-generated prediction.

The application collects user inputs, formats them into the expected feature structure, applies a previously fitted scaler, and passes the transformed data to the trained model.

---

## ✨ Features

- **Interactive UI:** A user-friendly interface developed with Streamlit.
- **Machine Learning Prediction:** Uses a trained KNN classification model.
- **Health Attribute Inputs:** Accepts multiple health-related parameters.
- **Feature Scaling:** Uses a pre-trained scaler to transform input features.
- **Categorical Feature Handling:** Formats categorical inputs using one-hot encoded columns.
- **Probability Display:** Displays an estimated prediction probability when supported by the model.
- **Modular Code:** Separates input collection, data preparation, artifact loading, and prediction logic.
- **Cached Model Loading:** Uses Streamlit's resource caching to avoid repeatedly loading model artifacts.

---

## 🧠 Input Features

The application accepts the following inputs:

| Feature | Description |
|---|---|
| Age | Age of the individual |
| Sex | Sex category |
| Chest Pain Type | Reported chest pain category |
| Resting Blood Pressure | Resting blood pressure in mm Hg |
| Cholesterol | Cholesterol level in mg/dL |
| Fasting Blood Sugar | Whether fasting blood sugar exceeds 120 mg/dL |
| Resting ECG | Resting electrocardiogram category |
| Maximum Heart Rate | Maximum heart rate achieved |
| Exercise-Induced Angina | Whether angina occurs during exercise |
| Oldpeak | ST depression value |
| ST Slope | Slope category of the ST segment |

These inputs are used by the application to prepare a feature vector compatible with the trained model.

---

## 🛠️ Technologies Used

- **Python** — Core programming language
- **Pandas** — Input data preparation
- **Scikit-learn** — Machine learning and preprocessing
- **Streamlit** — Web application interface
- **Joblib** — Loading serialized model artifacts

---

## 📂 Project Structure

```text
heartattackdetection/
│
├── app.py
├── knn_heart.pkl
├── scaler.pkl
├── columns.pkl
├── requirements.txt
├── README.md
└── .gitignore
```

**File descriptions:**

- `app.py` — Main Streamlit application.
- `knn_heart.pkl` — Saved, trained KNN classification model.
- `scaler.pkl` — Previously fitted feature scaler.
- `columns.pkl` — Expected feature column names and order.
- `requirements.txt` — Python dependencies.
- `README.md` — Project documentation.
- `.gitignore` — Files and directories Git should ignore.

*The project structure above assumes these files are present in the repository.*

---

## ⚙️ Installation and Setup

Follow these steps to run the application locally.

### 1. Clone the Repository

Replace `<your-github-username>` with your GitHub username.

```bash
git clone https://github.com/<your-github-username>/heartattackdetection.git
```

### 2. Navigate to the Project Directory

```bash
cd heartattackdetection
```

### 3. Create a Virtual Environment

For macOS and Linux:

```bash
python3 -m venv .venv
```

### 4. Activate the Virtual Environment

```bash
source .venv/bin/activate
```

### 5. Install Dependencies

If a `requirements.txt` file is available:

```bash
python -m pip install -r requirements.txt
```

Otherwise, install the main dependencies:

```bash
python -m pip install streamlit pandas scikit-learn joblib
```

**Important:** Use a compatible Python and Scikit-learn version for the versions used when saving the model and scaler. Serialized model artifacts may not work correctly across incompatible library versions.

### 6. Run the Application

```bash
streamlit run app.py
```

Streamlit will provide a local URL in your terminal, typically:

```text
http://localhost:8501
```

Open that address in your browser to interact with the application.

---

## 🔍 How It Works

The application follows these steps:

1. **Load Model Artifacts:** Loads the trained model, fitted scaler, and expected feature columns.
2. **Collect Inputs:** Presents an interactive form for entering health-related attributes.
3. **Prepare Input Data:** Converts the submitted values into a Pandas DataFrame.
4. **Align Features:** Adds missing expected columns with zero values and arranges the columns in the required order.
5. **Scale Features:** Applies the previously fitted scaler to the input data.
6. **Generate Prediction:** Passes the transformed input to the trained KNN classifier.
7. **Display Results:** Shows the predicted class and, when supported, an estimated probability.

---

## 📊 Machine Learning Model

The application currently loads a trained **K-Nearest Neighbors (KNN) classifier**.

KNN is a supervised machine learning classification algorithm that predicts a sample's class based on the classes of nearby samples in the feature space.

The application also uses a fitted scaler to transform input features before prediction.

**Note:** Any additional classification algorithms should be documented here only if they were actually trained and evaluated as part of this project.

---

## 🚀 Future Improvements

- Compare multiple classification algorithms using appropriate evaluation metrics.
- Add model evaluation results, including precision, recall, F1-score, and confusion matrix.
- Improve input validation and error handling.
- Add model interpretability features.
- Improve the application's visual design and accessibility.
- Deploy the application to a public hosting platform.
- Add automated tests for data preprocessing and prediction.

---

## ⚠️ Medical Disclaimer

This application is an educational machine learning project, not a clinically validated medical tool.

Predictions depend on the training dataset, preprocessing steps, and model performance. They may be inaccurate and should not be interpreted as a diagnosis or a substitute for advice from a qualified healthcare professional.

---

## 👨‍💻 Author

**Akarsh**

Aspiring AI Engineer | Machine Learning | Python

---

⭐ If you find this project interesting, feel free to explore the repository and share your feedback!
