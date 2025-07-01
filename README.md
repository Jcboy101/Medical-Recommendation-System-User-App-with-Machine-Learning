# 🧠 Medical Recommendation System

An AI-powered web platform that helps users understand potential illnesses based on symptoms, and delivers instant recommendations — medications, precautions, diet, and workout advice — all from a single input.

![image](https://github.com/user-attachments/assets/28688dde-c4af-4be7-8d38-f864096daa48)


---

## 📌 Overview

Millions of people suffer from **undiagnosed or misdiagnosed conditions**, often due to lack of access to timely medical guidance. The **Medical Recommendation System** aims to bridge that gap by providing an intelligent, easy-to-use interface where users can input symptoms and instantly receive:

- 🔍 A **likely diagnosis**
- 💊 Recommended **medications**
- 🛡️ Important **precautions**
- 🍲 Suggested **diets**
- 🏃‍♂️ Guided **workouts or lifestyle changes**

This is not a replacement for doctors — it's an assistive tool for early awareness and better decisions. [Click here](http://medrecommnsystem-env.eba-deq5y2eb.us-east-1.elasticbeanstalk.com/predict) to try live app


---

## 🎯 Purpose

The purpose of this system is to:
- 💡 **Empower individuals** with early insight into potential diseases.
- ⚕️ **Assist healthcare professionals** with a pre-diagnostic tool.
- 📚 **Educate users** on possible symptoms-disease relationships and healthy responses.
- 🌍 **Reduce diagnostic friction**, especially in underserved or remote areas.

---

## 🚨 The Problem

In many regions, individuals:
- Lack immediate access to healthcare
- Ignore or misinterpret their symptoms
- Depend on unverified online advice or self-medicate poorly

This leads to:
- Late diagnosis
- Worsened health conditions
- Higher treatment costs

---

## 💡 The Solution

This system uses a machine learning model trained on 132 symptoms mapped to 41 diseases. Combined with:
- A **fuzzy matching algorithm** to understand natural symptom input
- Rich, structured medical datasets (description, medication, diet, etc.)
- A **user-friendly Flask web interface**

It gives users a **quick, accessible, and informative diagnosis-like experience** in seconds.

---

## ⚙️ How It Works

1. User enters symptoms (e.g., _fever, headache, nausea_).
2. Symptoms are matched to known terms using **fuzzy matching**.
3. A **one-hot vector** is built for the model using matched symptoms.
4. The **trained SVM model** predicts the most likely disease.
5. Matching info is fetched from CSVs for:
   - 🔬 Disease description
   - 💊 Medications
   - 🛡️ Precautions
   - 🍽️ Diet
   - 🏃 Workouts
6. The result is rendered instantly in the browser.

---

## 🧪 Key Components

| Component       | Description |
|----------------|-------------|
| **ML Model**    | Trained SVC model (on ~5k entries) |
| **Fuzzy Matching** | Handles user input variation (e.g. "feverr" → "fever") |
| **Flask App**   | Backend serving routes and rendering predictions |
| **Datasets**    | 6 curated CSVs for full disease guidance |
| **Notebook**    | Jupyter notebook for training, tuning, and exporting the model |

---

## 🌟 Why This Project Matters

- ⏱️ Reduces the delay in taking early action
- 🌍 Accessible in low-resource settings
- 👩‍⚕️ Helps non-experts make informed decisions
- 📚 A solid foundation for a **telemedicine** or **health AI** system

---

## 🚀 Getting Started

### ✅ Prerequisites
```bash
pip install flask pandas numpy scikit-learn
```

### 🔧 Run the App
```bash
python app.py
```
Then visit `http://localhost:5000/` in your browser.

---

## 🧩 File Structure
```
├── app.py                        # Flask web application
├── svc.pkl                      # Trained SVC model
├── templates/
│   └── index.html               # Web UI
├── datasets/
│   ├── symptoms_df.csv
│   ├── description.csv
│   ├── medications.csv
│   ├── precautions_df.csv
│   ├── diets.csv
│   └── workout_df.csv
├── Medicine Recommendation System.ipynb   # Model training and export
```

---

## 🚀 Future Improvements

- ✅ REST API or mobile app version
- 🧑‍⚕️ Doctor-facing interface for reviewing user cases
- 📈 Disease probability scoring
- 🌐 Multilingual support
- 🔒 Privacy-focused login & history tracking

---

## 📄 Disclaimer

This tool is intended for educational and early awareness purposes only. It is **not a substitute** for professional diagnosis or treatment. Always consult with a certified healthcare provider.

---

