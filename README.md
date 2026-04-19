# BBS-Sleep-Quality-Prediction
Neural Network, Deep Learning, GRU Time Series model, on synthetic data. OPTUNA Hyperp. optimization 

# 😴 Sleep Quality Prediction
### Time-series forecasting using Deep Learning (GRU) and Bayesian Optimization (Optuna)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gvn414sWfIazjJFL1FOf6NmcIg7O9Hip)

## 📌 Project Overview
[cite_start]This project focuses on predicting sleep quality by analyzing sequential biometric and lifestyle data[cite: 1, 2]. [cite_start]We implemented a Recurrent Neural Network (RNN) to capture temporal dependencies in the data and optimize predictive accuracy[cite: 1, 2].

## 🧠 Model Architecture: GRU vs. LSTM
[cite_start]For this time-series task, we selected a **Gated Recurrent Unit (GRU)** over the traditional LSTM[cite: 1, 2].
* [cite_start]**Efficiency (Leaner):** A GRU is structurally simpler, featuring only two gates (reset and update) compared to the three gates in an LSTM.

* [cite_start]**Performance:** This "lean" architecture requires less computational power and memory, resulting in faster training times without sacrificing the ability to handle the vanishing gradient problem.
* [cite_start]**Suitability:** Given the dataset's characteristics, the GRU offers an ideal balance between model complexity and generalization capability.

## 🛠 Hyperparameter Optimization: Optuna vs. GridSearch
[cite_start]Rather than using an exhaustive and slow GridSearch, we utilized **Optuna** for model fine-tuning.
* [cite_start]**Bayesian Approach:** Optuna employs a probabilistic approach to "learn" from previous trials, quickly narrowing down the most promising regions of the search space.

* [cite_start]**Efficiency:** This allowed us to find the optimal combination of `hidden_size`, `num_layers`, and `learning_rate` in a fraction of the time required by traditional methods.

## 📊 Model Performance
[cite_start]Following optimization and final training, the model achieved the following results in predicting sleep quality:

* [cite_start]**Mean Squared Error ($MSE$):** `0.0193` (Measures the average squared difference between estimated and actual values).
* [cite_start]**Mean Absolute Error ($MAE$):** `0.1044` (Indicates the average magnitude of errors in a set of predictions).

[cite_start]The results demonstrate that the model accurately tracks sleep quality trends, successfully identifying underlying biometric patterns.

---
**DSBA Team - Deep Learning Project**
[cite_start]*Team Members: Filippo Iacchia, Alice, Nourhene, Malcolm Palmer.*
