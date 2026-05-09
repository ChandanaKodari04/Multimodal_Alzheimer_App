# 🧠 Multimodal Deep Learning System for Early Alzheimer’s Detection

This project implements a **Multimodal Deep Learning System** to detect **Alzheimer’s Disease** at an early stage using three independent modalities:

- 🧠 MRI Brain Images  
- 🗣 Speech Transcripts  
- 🧪 Cognitive Assessment Scores  

Each module predicts Alzheimer’s probability independently, and the results are combined using a **Weighted Decision-Level Fusion** approach to produce the final diagnosis.

The system is deployed using **Streamlit** for interactive user input and prediction.

---

# 📌 Project Overview

Alzheimer’s disease is a progressive neurological disorder that affects memory, reasoning ability, and language skills. Early detection is essential for improving patient care.

Traditional systems often rely on **single-modality data**, which may lead to incomplete diagnosis.

This project integrates:

- MRI imaging features  
- Speech-based linguistic features  
- Cognitive assessment scores  

to provide **more reliable and comprehensive predictions**.

---

# 🎯 Features

✅ Multimodal Alzheimer’s Detection  
✅ MRI Image Classification  
✅ Speech Transcript Analysis  
✅ Cognitive Score Prediction  
✅ Weighted Fusion Prediction  
✅ Streamlit-Based User Interface  
✅ Supports Partial Input (1, 2, or 3 modalities)

---

# 🧩 System Workflow

```
User Inputs
   │
   ├── MRI Module → MRI Probability
   │
   ├── Speech Module → Speech Probability
   │
   ├── Cognitive Module → Cognitive Probability
   │
   └── Weighted Fusion
            │
      Final Prediction
            │
       Streamlit Output
```

---

# 📂 Project Structure

```
project_folder/

├── app.py                     # Main Streamlit Application

├── utils/
│   ├── load_models.py        # Loads trained models
│
├── models/                   # Stored trained models
│   ├── mri_model.pth
│   ├── speech_model.pt
│   ├── cognitive_model.pkl
│
├── sample_inputs/            # Example test files
│
├── requirements.txt
│
└── README.md
```

---

# 🧠 Modules Description

---

# 1️⃣ MRI Module

### Model Type:
Deep Learning CNN Model

### Purpose:
Analyze MRI brain images to detect structural abnormalities associated with Alzheimer’s disease.

### Input:
- MRI image (.jpg / .png)

### Output:
- MRI Alzheimer’s Probability

---

# 2️⃣ Speech Module

### Model Type:
Transformer-based NLP Model (**BERT**)

### Purpose:
Analyze speech transcripts to detect linguistic abnormalities.

### Input:
- Speech transcript (.txt)

### Output:
- Speech Alzheimer’s Probability

---

# 3️⃣ Cognitive Module

### Model Type:
Machine Learning Model (**XGBoost**)

### Input Features:

- MMSE Score  
- ADAS-13 Score  
- FAQ Score  

### Output:
- Cognitive Alzheimer’s Probability

---

# 🔗 Multimodal Fusion

Final prediction is computed using:

```
Final Probability =

(Wm × PMRI + Wc × PCog + Ws × PSpeech)
/ (Wm + Wc + Ws)
```

Where:

- PMRI → MRI prediction  
- PCog → Cognitive prediction  
- PSpeech → Speech prediction  

Supports:

✔ Single Modality  
✔ Dual Modality  
✔ Full Multimodal Prediction  

---

# 🖥 Streamlit User Interface

The application allows users to:

- Upload MRI image  
- Upload speech transcript  
- Enter cognitive scores  
- Click Predict  
- View Alzheimer’s probability and diagnosis

---

# ⚙️ Installation Guide

Follow these steps to run the project locally.

---

# Step 1 — Clone Repository

```
git clone https://github.com/DMadhumita2904/multimodal-alzheimer-app.git

cd multimodal-alzheimer-app
```

---

# Step 2 — Create Virtual Environment

```
python -m venv venv
```

Activate environment:

### Windows

```
venv\Scripts\activate
```

### Linux / Mac

```
source venv/bin/activate
```

---

# Step 3 — Install Dependencies

```
pip install -r requirements.txt
```

---

# Step 4 — Run Streamlit App

```
streamlit run app.py
```

---

# 📦 Requirements

The following dependencies are required:

```
streamlit
torch
torchvision
transformers
scikit-learn
joblib
pandas
numpy
Pillow
gdown
```

Note:

`gdown` is used to download large model files if they are not present locally.

---

# 📥 Input Details

---

## MRI Input

- Format: `.jpg` or `.png`
- Preprocessed MRI brain slice

---

## Speech Input

Upload `.txt` file.

Example:

```
The boy is taking cookies from the jar.
The mother is washing dishes.
```

---

## Cognitive Input

Enter numeric values:

| Feature | Range |
|--------|-------|
| MMSE | 0–30 |
| ADAS-13 | 0–85 |
| FAQ | 0–30 |

---

# 📤 Output

The system returns:

- Alzheimer’s Probability Score  
- Final Prediction:

```
Normal
OR
Alzheimer’s Detected
```

---

# 🛠 Technologies Used

## Programming Language

Python

## Frameworks

- PyTorch  
- Transformers  
- Streamlit  

## Machine Learning

- Scikit-learn  
- XGBoost  

## Supporting Libraries

- Pandas  
- NumPy  
- Pillow  
- Joblib  
- gdown  

---

# 📊 Model Performance (Summary)

| Module | Model |
|--------|------|
| MRI | CNN-based Model |
| Speech | BERT Model |
| Cognitive | XGBoost |
| Fusion | Weighted Decision |

---

# 📄 Research Paper

**Title:**

Multimodal Alzheimer’s Disease Detection Using MRI, Cognitive Assessments, and Speech Analysis with Decision-Level Fusion

**Status:** Under Review

---

# 🔮 Future Work

- Add real-time speech recording  
- Integrate additional medical modalities  
- Improve model generalization  
- Deploy cloud-based version  

---

# ⚠️ Disclaimer

This project is intended for:

- Academic  
- Research  
- Demonstration purposes only  

It is **not intended for clinical diagnosis**.

---

# 👩‍💻 Contributors

- Dutta Krishna Madhumita — MRI Module  
- D Pravallika — Speech Module  
- Ghantasala Usha Sri — Dataset Management  
- Kodari Chandana — Cognitive Module  
- Janipalli Venkata Yamini — Deployment  

---

# 🙏 Acknowledgement

Developed under the guidance of:

**Dr. C P Pavan Kumar Hota**  
Assistant Professor  
Department of Artificial Intelligence  
SVECW, Bhimavaram

---
