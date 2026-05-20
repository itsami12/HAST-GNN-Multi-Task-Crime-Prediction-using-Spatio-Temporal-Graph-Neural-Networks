# A-EFN: Unified Detection of Deepfake and Fraudulent Audio in Emergency Communication Systems

## Overview

A-EFN (Advanced Equilibrium Field Network) is a multitask deep learning framework designed for:

- Audio Deepfake Detection
- Fake Emergency Call Detection
- Adversarial Robustness Evaluation

The framework combines equilibrium based representation learning with multitask classification to detect both AI generated speech and fraudulent emergency communication within a single architecture.

---

## Features

- Unified multitask framework
- Deepfake audio detection
- Fake emergency call detection
- Equilibrium based learning
- Focal loss optimization
- Conflict loss regularization
- FGSM adversarial robustness testing
- SMOTE balancing
- Audio augmentation
- Threshold optimization

---

## Datasets Used

### 1. Fake-or-Real (FoR)
Used for real and fake speech detection.

### 2. ASVspoof2019
Used for spoofed and AI generated speech detection.

### 3. 911 Recordings Dataset
Used for emergency fraud detection.

---

## Dataset Labels

| Label | Meaning |
|-------|---------|
| 0 | Real Audio |
| 1 | Deepfake / Spoofed Audio |
| 2 | Fake Emergency Call |

---

## Architecture

The proposed A-EFN architecture contains:

- Feature Projection Layer
- Equilibrium Energy Function
- Interaction Transformation Layer
- Deepfake Detection Head
- Fraud Detection Head
- Equilibrium Optimization Solver

---

## Feature Extraction

The framework extracts an 89 dimensional feature vector including:

- MFCC Mean
- MFCC Standard Deviation
- Spectral Contrast
- Zero Crossing Rate
- RMS Energy

---

## Data Augmentation

Fake emergency calls were augmented using:

- Noise Injection
- Pitch Shifting
- Time Stretching
- Volume Scaling

Augmentation factor:
- 36 fake emergency calls → 360 augmented samples

---

## Loss Functions

### Focal Loss
Used for handling class imbalance and difficult samples.

### Conflict Loss
Used for improving feature separation between classes.

---

## Hyperparameters

| Hyperparameter | Value |
|---|---|
| Learning Rate | 0.001 |
| Batch Size | 32 |
| Epochs | 35 |
| Optimizer | Adam |
| Hidden Dimension | 128 |
| Dropout | 0.5 |
| Scheduler | ReduceLROnPlateau |

---

## Results

### Deepfake Detection
- Accuracy: 98.11%
- ROC-AUC: 0.9987
- PR-AUC: 0.9989

### Fake Emergency Detection
- Accuracy: 96.21%
- ROC-AUC: 0.9919
- PR-AUC: 0.9207

---

## Adversarial Robustness (FGSM)

| Epsilon | Accuracy | F1 Score |
|---|---|---|
| 0.01 | 96.66% | 93.39% |
| 0.03 | 95.31% | 91.10% |
| 0.05 | 93.91% | 88.59% |

---

## Project Structure

```bash
A-EFN/
│
├── datasets/
├── models/
├── preprocessing/
├── feature_extraction/
├── training/
├── evaluation/
├── adversarial_testing/
├── results/
├── README.md
└── requirements.txt
```

---

## Installation

```bash
git clone https://github.com/yourusername/A-EFN.git

cd A-EFN

pip install -r requirements.txt
```

---

## Run Training

```bash
python train.py
```

---

## Run Evaluation

```bash
python evaluate.py
```

---

## Run Adversarial Testing

```bash
python fgsm_attack.py
```

---

## Research Contribution

This project introduces:

- First unified framework for deepfake and fake emergency detection
- Equilibrium based multitask learning
- Adversarial robustness evaluation for emergency audio
- Unified public dataset integration

---

## Future Work

Future work will focus on:

- Urdu paired audio-text datasets
- Pakistani emergency call datasets
- Real time deployment systems
- Multilingual deepfake detection
- Lightweight mobile deployment

---



FAST-NUCES Islamabad  
Department of Artificial Intelligence and Data Science

---

## License

This project is developed for research and academic purposes.
