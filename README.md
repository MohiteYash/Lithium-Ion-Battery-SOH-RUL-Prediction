# 🔋 Lithium-Ion Battery SOH & RUL Prediction  
### Deep Learning with CNN–RNN–Attention and Uncertainty Estimation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-TensorFlow-orange)
![Dataset DOI](https://img.shields.io/badge/Dataset-DOI-green)
![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)

An end-to-end deep learning framework for predicting **State of Health (SOH)** and  
**Remaining Useful Life (RUL)** of lithium-ion batteries using cycle-level
degradation data.

This project targets practical battery health monitoring for **Battery
Management Systems (BMS)** and predictive maintenance applications.

---

##  Key Features

- SOH prediction from historical battery cycle data  
- RUL prediction in remaining charge–discharge cycles  
- Hybrid **CNN–LSTM/RNN–Attention** deep learning architecture  
- Joint learning of SOH and RUL  
- Evaluation using standard error metrics (MAE, RMSE)  
- Scalable and deployment-ready pipeline  

---

## Problem Statement

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

## Model Architecture

The proposed framework consists of:

- **CNN** – Extracts local degradation-related features  
- **LSTM / RNN** – Models long-term temporal dependencies  
- **Attention Mechanism** – Emphasizes critical degradation stages  
- **Dual Output Heads** – Independent prediction of SOH and RUL  

<img width="7000" height="780" alt="image" src="https://github.com/user-attachments/assets/3a8ae1ba-a6c6-4140-8d70-900851bc8048" />

## Dataset

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

## Workflow

1. Dataset loading and preprocessing  
2. Feature normalization  
3. Time-series sequence generation  
4. Model training  
5. SOH and RUL prediction  
6. Performance evaluation  
7. Result visualization  

---

## Results

The performance of the proposed deep learning models was evaluated using  
**Mean Absolute Error (MAE)** and **Root Mean Square Error (RMSE)**.

### State of Health (SOH)

| Model | MAE | RMSE |
|------|-----|------|
| CNN–LSTM–Attention | 0.0759966731 | 0.0840301867 |

### Remaining Useful Life (RUL)

| Model | MAE (cycles) | RMSE (cycles) |
|------|--------------|---------------|
| CNN–RNN–Attention | 12.76664302 | 16.96857146 |

## 📈 Results Visualization and Analysis

<img width="691" height="393" alt="download" src="https://github.com/user-attachments/assets/b71df20a-8a31-4d0b-8030-6c13850de3db" />

This figure compares true SOH values with model predictions across test samples.
- The model successfully captures gradual SOH degradation trends
- Predicted SOH follows the true SOH trajectory with minimal lag
- Minor fluctuations occur during rapid degradation phases
Overall, the model demonstrates robust SOH estimation capability suitable for long-term battery health monitoring.

<img width="695" height="393" alt="download" src="https://github.com/user-attachments/assets/c72e766f-98e2-46a5-8241-43e8ab305709" />

This plot shows the true and predicted RUL values across test samples, along with a **±2σ confidence interval** obtained using uncertainty estimation.
- The predicted RUL closely tracks the true RUL trend
- Wider uncertainty bands appear near abrupt degradation regions
- Confidence intervals provide insight into prediction reliability,
  especially near end-of-life (EOL)
This uncertainty-aware prediction is valuable for risk-sensitive decision-making in Battery Management Systems (BMS).

<img width="463" height="470" alt="download" src="https://github.com/user-attachments/assets/c550a9ca-fc07-4b96-b4dd-6f07dfc0eec5" />

The scatter plot compares the predicted RUL values against the true RUL values for test samples. The red dashed diagonal line represents ideal predictions
(where predicted RUL equals true RUL).
- Most predictions closely follow the ideal diagonal trend
- Slight deviations are observed at very low and very high RUL values
- The model demonstrates strong correlation and low bias across the operating range
This indicates effective learning of nonlinear degradation behavior from cycle-level battery data.


> These results demonstrate effective modeling of nonlinear battery degradation
patterns. The attention mechanism improves prediction robustness, particularly
near end-of-life (EOL) regions.


