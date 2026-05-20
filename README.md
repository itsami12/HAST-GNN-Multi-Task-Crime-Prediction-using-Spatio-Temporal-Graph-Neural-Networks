# HAST-GNN: Multi-Task Crime Prediction using Spatio-Temporal Graph Neural Networks

HAST-GNN (Hierarchical Adaptive Spatio-Temporal Graph Neural Network) is a deep learning framework designed for multi-task crime prediction, hotspot forecasting, and urban crime analysis using large-scale spatio-temporal crime datasets. The framework combines temporal attention learning, hierarchical graph aggregation, crime-type interaction modeling, and multitask optimization for intelligent crime forecasting in large urban environments of the United States.

The proposed architecture was evaluated using the Chicago Crime Dataset containing approximately 7.69 million crime events collected between 2001 and 2025 across 77 community areas.

---

# Features

- Multi-task crime prediction framework
- Crime hotspot detection
- Hotspot location prediction
- Crime type classification
- Crime-hour forecasting
- Crime count prediction
- Crime trend prediction
- Hierarchical graph learning
- Temporal attention learning
- Adaptive crime-type interaction modeling
- Large-scale spatio-temporal crime forecasting

---

# Architecture

The proposed HAST-GNN architecture consists of the following major components:

## 1. Input Projection Layer
Transforms raw crime features into higher-dimensional latent representations.

## 2. ARATA Temporal Learning Module
Adaptive Retentive Attention Temporal Aggregation module for capturing short-term and long-term temporal crime dependencies.

## 3. CTIG Crime-Type Interaction Graph
Models hidden relationships and interactions between different crime categories.

## 4. AHG Hierarchical Graph Layer
Performs hierarchical graph learning using:
- Fine-grained community graph
- Coarse district-level graph

## 5. MAMTO Multi-Task Output Framework
Handles multiple prediction tasks simultaneously including:
- Hotspot detection
- Crime type prediction
- Crime-hour prediction
- Crime count forecasting
- Crime trend prediction

---

# Dataset

The framework uses the official Chicago Crime Dataset:

Dataset: Crimes - 2001 to Present  
Source: Chicago Police Department  
Records: ~7.69 million crime events  
Coverage: 2001 – 2025  
Community Areas: 77  

Dataset Link:
https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2

---

# Data Preprocessing

The preprocessing pipeline includes:

- Missing value removal
- Temporal feature extraction
- Community-area aggregation
- Rolling statistical features
- Crime-type encoding
- Crime-hour bucket generation
- Spatial feature engineering
- Temporal sequence generation
- Feature normalization using StandardScaler

Generated Features:
- Temporal features
- Spatial features
- Crime-type features
- Rolling trend statistics
- Hour-bucket distributions
- Location-specific crime frequencies

Total Engineered Features: 88

---

# Model Configuration

| Hyperparameter | Value |
|---|---|
| Hidden Dimension | 96 |
| Batch Size | 16 |
| Epochs | 120 |
| Learning Rate | 0.0002 |
| Weight Decay | 0.0001 |
| Optimizer | AdamW |
| Scheduler | OneCycleLR |
| Graph Attention Heads | 4 |
| Graph Layers | 3 |
| Dropout | 0.30 |
| Sequence Length | 60 |
| Crime Classes | 10 |
| Hour Buckets | 8 |

---

# Final Results

## Hotspot Detection
- ROC-AUC: 0.9495
- F1 Score: 0.7591

## Hotspot Location Prediction
- Haversine MAE: 1.39 km
- Within 1 km Accuracy: 75.5%

## Crime Type Prediction
- Accuracy: 60.17%
- Weighted F1 Score: 0.6534

## Crime-Hour Prediction
- Accuracy: 54.38%
- Weighted F1 Score: 0.5501

## Crime Count Forecasting
- Pearson Correlation: 0.8529
- Count MAE: 2.69 crimes/day

## Crime Trend Prediction
- Accuracy: 94.25%

---

# Installation

```bash
git clone https://github.com/your-username/HAST-GNN.git
cd HAST-GNN
pip install -r requirements.txt
```

---

# Requirements

```bash
torch
torch-geometric
numpy
pandas
scikit-learn
matplotlib
networkx
scipy
tqdm
```

---

# Run Training

```bash
python train.py
```

---

# Run Evaluation

```bash
python evaluate.py
```

---

# Project Structure

```bash
HAST-GNN/
│
├── data/
├── models/
├── preprocessing/
├── graphs/
├── training/
├── evaluation/
├── results/
├── utils/
├── train.py
├── evaluate.py
├── requirements.txt
└── README.md
```

---

# Research Contributions

- Proposed a unified multi-task crime forecasting framework
- Combined temporal attention with hierarchical graph learning
- Modeled crime-type interactions dynamically
- Performed simultaneous hotspot and crime forecasting
- Evaluated on large-scale real-world U.S. crime dataset
- Improved spatio-temporal crime understanding using multitask optimization

---

# Limitations

- Lower-frequency hour intervals such as 3–6h and 6–9h were more difficult to predict accurately
- Exact street-level coordinates were not available due to dataset privacy protection
- Fixed 60-day temporal windows may not fully capture adaptive crime behaviors

---



---

# License

This project is released under the MIT License.

---

# Acknowledgment

This research utilized the Chicago Crime Dataset provided by the Chicago Police Department and City of Chicago Data Portal.   
