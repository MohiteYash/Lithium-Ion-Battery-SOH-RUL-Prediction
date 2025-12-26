# 🔋 Lithium-Ion Battery SOH & RUL Prediction  
### Deep Learning with CNN–RNN–Attention and Uncertainty Estimation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-TensorFlow-orange)
![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF)
![Status](https://img.shields.io/badge/Status-Research%20Ready-success)

---

## 📌 Project Description

This repository provides a **complete, end-to-end deep learning framework** for predicting the **State of Health (SOH)** and **Remaining Useful Life (RUL)** of lithium-ion batteries using **real experimental aging data**.

The project focuses on:
- Battery degradation modeling using time-series data  
- Attention mechanisms to identify important degradation stages  
- Uncertainty estimation for safer and more reliable predictions  

This work is suitable for **battery prognostics and health management (PHM)** applications such as:
- Electric Vehicles (EVs)
- Energy Storage Systems (ESS)
- Predictive Maintenance
- Battery Management Systems (BMS)

---

## ✨ Key Features

- Real-world battery aging data (NASA dataset)
- Cycle-level feature engineering
- CNN–LSTM–Multi-Head Attention for SOH estimation
- CNN–RNN–Multi-Head Attention for RUL prediction
- Monte-Carlo Dropout for uncertainty estimation
- Reproducible, research-ready pipeline
- Kaggle-compatible implementation

---

## 📂 Dataset Information

- **Dataset:** NASA Lithium-Ion Battery Aging Dataset  
- **Format:** Preprocessed cycle-level CSV  
- **Platform:** Kaggle  

### Dataset Path (Kaggle)
```text
/kaggle/input/nasa-battery-cycle-level-dataset/
battery_cycle_level_dataset_CLEAN_FINAL.csv
