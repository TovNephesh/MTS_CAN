# Multivariate Time Series Intermittent Fault Detectionin Controller Area Network CAN
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
   

## Usage

### Data Preparation

The dataset used in this project consists of CAN log files, converted into structured time series format, with fault injection information provided. This allows for training and testing of models on real-time streaming data.

### Running the Benchmarking Experiment

To benchmark models across different TSCV methods:

1. **Walk-Forward Validation**: Each fold uses prior observations for training and future observations for testing.
2. **Sliding Window Validation**: A fixed-size window is moved across the dataset with a predefined step size, creating overlapping segments for training and testing.
3. **Blocking Window Validation**: A non-overlapping window approach, where each window covers a unique segment of the dataset, used for training and testing.

To run the experiments, execute the main benchmarking script:

```bash
python benchmark.py --model <model_name> --method <tscv_method>
