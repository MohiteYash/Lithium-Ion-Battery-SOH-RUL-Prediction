# 🔋 Lithium-Ion Battery SOH & RUL Prediction  
### Deep Learning with CNN–RNN–Attention and Uncertainty Estimation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-TensorFlow-orange)
![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF)
![Status](https://img.shields.io/badge/Status-Research%20Ready-success)

An end-to-end deep learning framework for predicting **State of Health (SOH)** and  
**Remaining Useful Life (RUL)** of lithium-ion batteries using cycle-level
degradation data.

This project targets practical battery health monitoring for **Battery
Management Systems (BMS)** and predictive maintenance applications.

---

## 🚀 Key Features

- SOH prediction from historical battery cycle data  
- RUL prediction in remaining charge–discharge cycles  
- Hybrid **CNN–LSTM/RNN–Attention** deep learning architecture  
- Joint learning of SOH and RUL  
- Evaluation using standard error metrics (MAE, RMSE)  
- Scalable and deployment-ready pipeline  

---

## ❓ Problem Statement

Lithium-ion batteries degrade due to electrochemical aging, thermal stress,
and operational variability. Accurate estimation of **SOH** and **RUL** is
critical for ensuring safety, reliability, and cost-effective operation in:

- Electric Vehicles (EVs)  
- Energy storage systems  
- Predictive maintenance frameworks  

Conventional model-based methods struggle with nonlinear degradation behavior.
This project applies deep learning to directly learn degradation patterns from
battery aging data.

---

## 🏗️ Model Architecture

The proposed framework consists of:

- **CNN** – Extracts local degradation-related features  
- **LSTM / RNN** – Models long-term temporal dependencies  
- **Attention Mechanism** – Emphasizes critical degradation stages  
- **Dual Output Heads** – Independent prediction of SOH and RUL  

<img width="7000" height="780" alt="image" src="https://github.com/user-attachments/assets/3a8ae1ba-a6c6-4140-8d70-900851bc8048" />

## 📂 Dataset

This project uses a publicly available lithium-ion battery degradation dataset
hosted on Kaggle and referenced using a permanent Digital Object Identifier (DOI).

**Dataset DOI:**  
https://doi.org/10.34740/kaggle/dsv/14272939

### Dataset Details
- Cycle-level lithium-ion battery aging data  
- Measured parameters include:
  - Voltage  
  - Current  
  - Temperature  
  - Capacity  
- Format: CSV (converted from original MAT files)  
- Train–test split performed at **battery level** to avoid data leakage  

---

## 🔄 Workflow

1. Dataset loading and preprocessing  
2. Feature normalization  
3. Time-series sequence generation  
4. Model training  
5. SOH and RUL prediction  
6. Performance evaluation  
7. Result visualization  

---

## 📊 Results

The performance of the proposed deep learning models was evaluated using  
**Mean Absolute Error (MAE)** and **Root Mean Square Error (RMSE)**.

### 🔋 State of Health (SOH)

| Model | MAE | RMSE |
|------|-----|------|
| CNN–LSTM–Attention | 0.0759966731 | 0.0840301867 |

### ⏳ Remaining Useful Life (RUL)

| Model | MAE (cycles) | RMSE (cycles) |
|------|--------------|---------------|
| CNN–RNN–Attention | 12.76664302 | 16.96857146 |

> These results demonstrate effective modeling of nonlinear battery degradation
patterns. The attention mechanism improves prediction robustness, particularly
near end-of-life (EOL) regions.


