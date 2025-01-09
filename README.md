# Multivariate Time Series Intermittent Fault Detection in Controller Area Network (CAN)

Fault detection in Controller Area Network (CAN) systems is crucial for ensuring the reliability and safety of automotive and industrial applications. This project investigates and compares the effectiveness of time series classification models for supervised fault detection in CAN data.

## Overview

This repository contains the code and data for a benchmarking experiment aimed at detecting intermittent faults in automotive Controller Area Network (CAN) data. The primary objective of this project is to evaluate and compare various machine learning (ML) and deep learning (DL) models using different Time Series Evaluation techniques. These experiments are designed to assess model performance in streaming environments with temporal dependencies.

### Key Features

- **Time Series Evaluation Strategies**: 
  - **Holdout**: Divides the dataset into a single training set and a testing set, providing a baseline for comparison.
  - **Walk-Forward Validation**: Sequentially expands the training set with each fold while testing on the immediate future observations.
  - **Sliding Window Validation**: Uses a fixed-size window that moves across the dataset with overlapping segments for training and testing.
  
- **Machine Learning and Deep Learning Models**: 
  - **Traditional ML**: XGBoost, Random Forest, and Support Vector Machines.
  - **Deep Learning Models**: LSTM-FCN, ResNet, InceptionTime, and TCN.

- **Evaluation Metrics**:
  - Accuracy, Precision, Recall, F1-Score, AUC-ROC, and Matthews Correlation Coefficient (MCC).

---

## Installation

### Prerequisites
- Python 3.8 or higher.
- Required Python libraries are listed in the `requirements.txt` file.

### Steps
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/TovNephesh/Multivariate-Time-Series-Intermittent-Fault-Detection-in-Controller-Area-Network-CAN-)

To run the experiments, execute the main benchmarking script:

```bash
python benchmark.py --model <model_name> --method <tscv_method>
