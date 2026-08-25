# Predicting Drug Solubility in Supercritical Carbon Dioxide Using Neural Networks

A machine learning regression project using an Artificial Neural Network (ANN) to predict drug solubility in supercritical carbon dioxide (scCO₂) from experimental process and molecular properties.

## 📌 Project Overview

Solubility in supercritical carbon dioxide is an important parameter in pharmaceutical processing, with applications in drug formulation, extraction and purification.

This project explores the use of neural networks to model the relationship between operating conditions, drug properties and solubility. The objective was to develop and evaluate a neural network regression model capable of predicting drug solubility from experimental data.

The project covers the complete machine learning workflow, from data exploration and preprocessing to model development, training and evaluation.

## 🎯 Objectives

- Explore a dataset of drug solubility measurements in supercritical CO₂.
- Analyse relationships between process and molecular properties.
- Preprocess and scale the input data for neural network training.
- Develop an Artificial Neural Network for regression.
- Evaluate model performance using MAE, MSE and R².
- Visualise training behaviour and predicted versus actual solubility values.

## 📊 Dataset

The dataset was obtained from Kaggle and contains experimental information related to drug dissolution in supercritical carbon dioxide.

The dataset contains **2,134 observations** and includes variables such as:

| Feature | Description |
|---|---|
| `temp` | Temperature |
| `press` | Pressure |
| `mw_drug` | Drug molecular weight |
| `mp_drug` | Drug melting point |
| `rho_scco2` | Supercritical CO₂ density |
| `sol` | Solubility |
| `sol_mol_frac` | Solubility expressed as mole fraction |

The dataset is included in this repository for reproducibility.

## 🔬 Methodology

The project follows these main steps:

1. **Data loading and exploration**
   - Imported the dataset using Pandas.
   - Inspected data types, descriptive statistics and distributions.
   - Explored relationships between variables using visualisations and correlation analysis.

2. **Data preprocessing**
   - Prepared the input features and target variable.
   - Split the data into training and test sets.
   - Scaled the input features before training the neural network.

3. **Neural network development**
   - Built a feed-forward Artificial Neural Network using Keras.
   - Used ReLU activation functions in the hidden layers.
   - Used a linear output layer because solubility is a continuous regression target.

4. **Model training**
   - Optimised the model using Adam.
   - Used Mean Squared Error as the loss function.
   - Trained the model for 100 epochs with a batch size of 32.

5. **Model evaluation**
   - Generated predictions on the test set.
   - Evaluated performance using:
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - R² score
   - Compared predicted and actual solubility values visually.

## 🧠 Neural Network Architecture

The model consists of:

```text
Input Features
      ↓
Dense Layer — 64 neurons, ReLU
      ↓
Dense Layer — 64 neurons, ReLU
      ↓
Output Layer — 1 neuron, Linear
