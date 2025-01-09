# Multivariate Time Series Intermittent Fault Detection in Controller Area Network (CAN)

In recent years, the rapid growth of interconnected systems has resulted in the generation of vast amounts of time series data across various domains. In the automotive sector, Controller Area Network (CAN) bus data represents a complex multivariate time series (MTS) that captures interactions among electronic control units (ECUs) to enable real-time communication and ensure vehicle reliability and safety. This dynamic data encapsulates information such as engine performance, sensor readings, and operational status, offering critical insights into a vehicle’s health. Anomalies in CAN data (represented as intermittent faults) can indicate potential malfunctions or security threats, thus making fault detection a crucial task for modern automotive systems.

This study benchmarks eight state-of-the-art machine learning (ML) models for supervised fault detection in CAN data and focuses on the unique challenges posed by temporal dependencies and intermittent fault occurrences. Using three time series evaluation strategies (holdout, walk-forward, and sliding window), we evaluate the models' performance under varying k-fold splits. Our contributions include insights into the role of temporal structure in fault detection, the effect of cross-validation strategies on model performance, and a publicly available CAN dataset with labeled fault zones for reproducibility. This repository provides the tools and resources needed to advance fault detection research in CAN systems.

## Overview

This repository contains the code for a benchmarking experiment aimed at detecting intermittent faults in automotive CAN data. The primary objective of this project is to evaluate and compare various ML models using different time series evaluation techniques. These experiments are designed to assess model performance in streaming environments with temporal dependencies.

### Key Features

- **Time Series Evaluation Strategies**: 
  - **Holdout**: Divides the dataset into a single training set and a testing set, providing a baseline for comparison.
  - **Walk-Forward Validation**: Sequentially expands the training set with each fold while testing on the immediate future observations.
  - **Sliding Window Validation**: Uses a fixed-size window that moves across the dataset with overlapping segments for training and testing.
  
- **Machine Learning Models**: 
  - **Shallow ML**: XGBoost, Random Forest, and Support Vector Machines.
  - **Deep Learning**: LSTM-FCN, ResNet, InceptionTime, ROCKET, and TCN.

- **Evaluation Metrics**:
  - Accuracy, Precision, Recall, F1-Score, AUC-ROC, and Matthews Correlation Coefficient (MCC).

---

## Installation

### Prerequisites
- Python 3.8 or higher.
- Required Python libraries are listed in the `requirements.txt` file.

### Steps


---
## Dataset
A detailed overview of the dataset can be found at You can download the dataset from [Zenodo](https://zenodo.org/records/12807317). The dataset is comprised of the MTS data from a real CAN bus, specifically designed for fault detection research. It includes labeled instances of both normal and faulty operations, facilitating the development and evaluation of ML models for identifying anomalies in automotive systems. This resource can be used by researchers and practitioners aiming to enhance vehicle safety and reliability through advanced fault detection methodologies.
