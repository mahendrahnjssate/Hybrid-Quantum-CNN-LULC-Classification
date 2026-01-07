# Hybrid-Quantum-CNN-LULC-Classification
# Hybrid-QCNN-LULC

This repository provides the implementation of **Classical CNN, Quantum CNN (QCNN), and Hybrid Quantum–Classical CNN (Hybrid QCNN)** models for **Land Use / Land Cover (LULC) classification** using multispectral satellite imagery.

The code is shared to ensure **reproducibility, transparency, and ease of validation** of the results reported in the associated research work.

---

## LULC Classes

The models perform **four-class LULC classification**:

| Label | Class Name        |
|------:|-------------------|
| 0     | Built-up area     |
| 1     | Vegetation        |
| 2     | Water bodies      |
| 3     | Others land       |

---

## Implemented Models

- **Classical CNN**  
  A standard convolutional neural network used as a baseline for comparison.

- **QCNN (Quantum CNN)**  
  A fully quantum feature extraction model using:
  - ZFeatureMap-based data encoding  
  - Parameterized RX–RY–RZ quantum convolution  
  - Localized CNOT entanglement  
  - Pauli-Z measurement

- **Hybrid QCNN**  
  A hybrid quantum–classical architecture that combines quantum feature extraction with classical dense layers, making it suitable for NISQ-era devices.

---

## Quantum Framework

Quantum circuits are implemented using:

- **PennyLane** quantum machine learning framework  
- Noiseless quantum simulator (`default.qubit`)  
- Hybrid quantum–classical optimization via parameter-shift differentiation  

---

## Repository Contents

- `hybrid_qcnn_lulc.py`  
  A single, self-contained Python script implementing:
  - Classical CNN  
  - QCNN  
  - Hybrid QCNN  
  - Patch-based inference (128 × 128)  
  - Color-coded LULC classification maps

- `README.md`  
  Project description and usage instructions

---

## How to Run

### Step 1: Install dependencies
```bash
pip install torch torchvision numpy matplotlib opencv-python pennylane
