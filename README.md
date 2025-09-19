# IBM‑Cloud‑Project: Power System Fault Detection & Classification

## Description  
Detect faults (e.g., short‑circuit, open‑circuit) in power systems using voltage/current signature data and ML models deployed via IBM Cloud Watson ML.

## Table of Contents  
1. Prerequisites  
2. Installation  
3. Usage  
4. Model & Evaluation  
5. IBM Cloud Deployment  
6. Project Structure

---

## Prerequisites
- Python 3.8+  
- IBM Cloud Lite with Watson Studio & Watson Machine Learning (watsonx.ai Runtime)  
- API Key, Workspace & Deployment Space configured  
- Optional: `conda env export` or `.env` for credentials

## Installation
```bash
git clone https://github.com/your‑username/IBM‑Cloud‑Project.git
cd IBM‑Cloud‑Project
pip install -r requirements.txt
```

## Training
python src/train_model.py --data data/fault_dataset.csv

## Evaluation
python src/evaluate.py

## import requests
payload = {"features": [...]}
response = requests.post("<IBM_ML_endpoint>", json=payload, headers={"Authorization": "Bearer <token>"})
print("Predicted fault type:", response.json())

## Project Structure
├── data/
│   └── fault_dataset.csv
├── notebooks/
│   └── FaultDetection.ipynb
├── src/
│   ├── preprocess.py
│   ├── train_model.py
│   ├── evaluate.py
│   ├── deploy_ibm.py
├── requirements.txt
└── README.md
