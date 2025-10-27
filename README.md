# 🩺 Medical Diagnosis System using Fuzzy Logic Controller

This project implements an intelligent **Medical Diagnosis System** using a **Fuzzy Logic Controller (FLC)** developed in **MATLAB**.  
It simulates the reasoning of medical experts by analyzing patient symptoms and predicting the likelihood of common diseases.

---

## 📘 Project Overview
Traditional medical diagnosis often faces challenges due to uncertain, overlapping, or imprecise symptoms.  
This project addresses that problem using **Fuzzy Logic**, which allows decision-making with partial truth values—similar to human reasoning.

The system uses a **Mamdani-type Fuzzy Inference System (FIS)** built in MATLAB’s **Fuzzy Logic Toolbox** to model the diagnostic process.

---

## ⚙️ System Design

### Components
1. **Fuzzification** – Converts numeric symptom data into linguistic variables (e.g., *Low, Moderate, High*).  
2. **Inference Engine** – Applies a set of fuzzy “IF–THEN” rules based on medical expertise.  
3. **Defuzzification** – Converts fuzzy results into a crisp disease likelihood value.

### Inputs (Symptoms)
- Temperature (°F)  
- Headache  
- Joint/Muscle Pain  
- Abdominal Pain  
- Vomiting  
- Dark Urine  
- Yellow Eyes  
- Cough (Duration-based)  
- Other symptoms (Chills, Dehydration, Cramping, Pain behind eyes, etc.)

### Outputs (Diseases)
- Viral Fever  
- Dengue Fever  
- Hepatitis  
- Tuberculosis  
- Malaria  
- Diarrhea  

---

## 🧠 Fuzzy Rule Base
The rule base is designed using medical knowledge.  
Example:
IF Temperature is High AND Headache is Yes AND Vomiting is Yes
THEN Disease is Viral Fever.
The system uses the **MIN–MAX** method for rule evaluation in the Mamdani inference model.

---

## 🧪 Results & Discussion
- Simulations performed using MATLAB’s **Rule Viewer** and **Surface Viewer**.  
- The system provides **smooth**, **logical**, and **human-like** diagnostic outputs.  
- Effectively handles uncertain or overlapping symptoms.  
- Demonstrates fuzzy logic’s strength in **medical decision support systems**.

---

## 🩻 Conclusion
The project successfully models a **Fuzzy Logic–based Medical Diagnosis System** that can:
- Predict diseases based on multiple symptoms  
- Support doctors and health workers in early disease detection  
- Operate efficiently even with uncertain input data  

🔮 **Future Scope:**
- Integrate **machine learning** for adaptive rule updates  
- Develop a **mobile health (mHealth)** application for real-time diagnosis

---

## 💡 Usage
To open and test the fuzzy system:
matlab
fuzzyLogicDesigner('research_final_1.fis')

Or, use programmatically:

fis = readfis('research_final_1.fis');
output = evalfis(fis, [temperature, headache, jointPain, ...]);
