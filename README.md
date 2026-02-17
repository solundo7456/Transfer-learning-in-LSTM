# Transfer-learning-in-LSTM

This project focuses on predicting blood glucose levels using time-series LSTM models and transfer learning, applied to continuous glucose monitoring data. The workflow is designed to leverage historical data while efficiently adapting to new weekly measurements.

Workflow Overview

Baseline Model Training

Trained on the first 3 months of patient glucose data.
LSTM architecture captures temporal dependencies in glucose patterns.

Transfer Learning with Gaps

Data includes a gap period after the initial 3 months to simulate realistic scenarios.

The model is fine-tuned on new weekly data without forgetting previously learned patterns.
Gradual unfreezing of LSTM layers allows controlled adaptation.

Incremental Training

New weekly data is added sequentially, enabling the model to improve predictions as more data becomes available.
Feature scaling, sequence creation, and data optimization pipelines support this incremental update.

Hyperparameter Tuning

Learning rates for LSTM layers and the fully connected layer, along with weight decay, are optimized using grid/random search.
Metrics tracked include MSE, RMSE, MAE, and R².

Key Features

Handles time-series glucose data efficiently.
Uses transfer learning to leverage prior knowledge.
Supports gradual unfreezing for fine-tuning without overfitting.
Automates data preprocessing, scaling, and sequence generation.
Provides performance tracking and hyperparameter optimization.

Tech Stack
Python 3.10
PyTorch for LSTM modeling
Pandas & NumPy for data handling
scikit-learn for preprocessing and scaling

Jupyter Notebook for experimentation
