# Multivariate-Time-Series-Intermittent-Fault-Detection-in-Controller-Area-Network-CAN-
Fault detection in Controller Area Network (CAN) systems is crucial for ensuring the reliability and safety of automotive and industrial applications. This study investigates and compares the effectiveness of time series classification models for supervised fault detection in CAN data

## Overview

This repository contains the code and data for our benchmarking experiment aimed at detecting intermittent faults in automotive Controller Area Network (CAN) data. The goal of this project is to compare various machine learning (ML) and deep learning (DL) models using different Time Series Cross-Validation (TSCV) techniques to evaluate their effectiveness in a streaming environment for fault detection.

### Key Features
- **TSCV Strategies**: Implements three different TSCV techniques (Walk-Forward, Blocking Window, Sliding Window) to respect temporal dependencies in the data.
- **ML and DL Models**: Benchmarks 8 models, including both traditional machine learning algorithms (e.g., XGBoost, Random Forest) and advanced deep learning models (e.g., LSTM, ResNet, InceptionTime).
- **Evaluation Metrics**: Performance is evaluated using metrics such as Accuracy, Precision, Recall, F1-Score, AUC-ROC, and Matthews Correlation Coefficient (MCC).

---

## Installation

1. Clone the repository:
   ```bash
   

