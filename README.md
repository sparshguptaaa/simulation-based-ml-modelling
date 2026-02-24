# Data Generation Using Simulation for Machine Learning  
## Predicting CartPole Stability Using OpenAI Gym

---

## 📌 Assignment Overview

This project demonstrates how **simulation-based modelling** can be used to generate synthetic data for **machine learning applications**.  
A physics-based simulator is used to generate data through an API, and this data is then used to formulate and solve a **supervised machine learning problem**.

## 🎯 Problem Statement

**Predict the stability duration of a CartPole system based on its initial physical state.**

More specifically:

- Given the **initial state of the CartPole system**, predict how long the pole will remain balanced before failure.
- Stability duration is measured as the **total episode reward**, which corresponds to the number of time steps the system remains stable.

---

## 🧪 Simulator Used

### OpenAI Gym – CartPole-v1

---

## 📊 Dataset Description

### Input Features
The initial state returned by the simulator consists of:
- Cart position
- Cart velocity
- Pole angle
- Pole angular velocity

### Target Variable
- Episode reward (proxy for system stability duration)

### Dataset Size
- 1000 simulation episodes

---

## 🤖 Machine Learning Task

The generated dataset is used to train and evaluate multiple **supervised regression models**.

### Models Evaluated
- Linear Regression
- Ridge Regression
- K-Nearest Neighbors (KNN)
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

All models are trained on the same dataset and evaluated under identical conditions.

---

## 📈 Evaluation Metrics

Model performance is evaluated using:
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

These metrics quantify prediction accuracy and the ability of each model to explain variance in the target variable.

---

## 🔍 Key Results & Observations

- Nonlinear models (KNN and tree-based ensembles) significantly outperform linear models.
- Linear regression performs poorly due to the highly nonlinear and chaotic dynamics of the CartPole system.
- KNN achieved the best overall performance, indicating strong local nonlinear relationships in the simulator-generated data.

These results highlight the importance of **model selection** when learning from simulation-based datasets.

---
