# ❤️ Predictive Modeling for Early Detection of Heart Attack Risk 28/12/2024

This project uses machine learning to predict the likelihood of heart attack based on patient health indicators. Our goal is to support early diagnosis and intervention through AI-powered decision tools for healthcare providers.

## 🎯 Objectives

- Analyze patient health data to detect heart attack risk early.
- Build a machine learning model that classifies patients as high or low risk.
- Deploy an interactive Gradio app for real-time prediction and decision support.

---

## 🧠 Business Understanding

Heart disease is the leading cause of global mortality. Diagnosis is often delayed due to a lack of AI integration in the healthcare system. This project aims to:

- Help physicians prioritize high-risk individuals.
- Reduce healthcare costs through early prevention.
- Empower patients and healthcare stakeholders with actionable insights.

---

## 📊 Dataset Summary

- **Source**: [Kaggle – Heart Disease Indicators 2022](https://www.kaggle.com/datasets) `heart_2022_with_nans.csv`
- **Size**: 445,132 respondents, 40 attributes
- **Key Features**: Age, Gender, BMI, smoking, physical activity, general health, and disease history
- **Preprocessing Steps**:
  - Missing value imputation
  - Categorical encoding
  - Removal of unrealistic height/weight values
  - Feature selection and filtering

---

## 🤖 Models Evaluated

| Model             | Accuracy | Key Notes                                      |
|------------------|----------|------------------------------------------------|
| Support Vector Machine (SVM) | 82%      | Strong for high-dimensional data            |
| AdaBoost          | 84%      | Performs well with weak learners              |
| **Random Forest** | **85%**  | Best overall performance, selected for deployment |

📌 **Random Forest was selected as the final model** due to its high accuracy and robustness.
---

## 🚀 Deployment Quick Start (Gradio in Google Colab)

Launch the Gradio app **without retraining the model** by following these steps:

### 🛠️ Steps:
1. Open the notebook: `Heart_Attack_Predictor.ipynb` in **Google Colab**
2. Upload the file `random_forest_model.zip` into the Colab runtime
3. Unzip it using:

   ```python
   import zipfile
   with zipfile.ZipFile("random_forest_model.zip", 'r') as zip_ref:
       zip_ref.extractall()
   
4. Skip the model training section and scroll to the **Gradio deployment** section  
5. Run the cell to launch the Gradio app  
6. Input patient data and receive a prediction: **"High Risk"** or **"Low Risk"**

---

## 🧪 Testing the Model

You can simulate real-world predictions by manually entering values into the Gradio interface.

### Key Features:
- Age  
- BMI  
- Physical activity  
- General health  
- Disease history (stroke, diabetes, etc.)  
- Smoking and alcohol consumption  

> The output helps assess whether a patient is at high risk of heart attack based on their health indicators.

---

## 🏥 Stakeholder Impact

- **Hospitals & Clinics**: Improve triage and decision-making efficiency  
- **Patients**: Receive timely and targeted medical attention  
- **Insurance Providers**: Reduce costs by supporting early preventive care  
- **Policy Makers**: Better allocate healthcare resources using predictive insights  

---

## 🔮 Future Enhancements

- Host the Gradio demo on **Hugging Face Spaces** for 24/7 accessibility  
- Integrate with **Electronic Health Record (EHR)** systems  
- Incorporate **explainable AI** (e.g. SHAP values)  
- Add dashboards for visualizing predictions and trends  
- Retrain periodically based on updated patient data and trends 

---

## 👥 Team

This project was completed as part of the WQD7003 *Data Analytics* course by **Data Glam Squad** in 28 December 2024.

---

### 📄 License

This project is for academic purposes only.
