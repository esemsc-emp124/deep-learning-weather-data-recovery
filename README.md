# Deep Learning for Weather Data Reconstruction

This project was developed as part of the **Deep Learning module** in the MSc *Applied Computational Science and Engineering* at **Imperial College London**. It was completed under a **24-hour assessment constraint**, simulating real-world time-limited project execution.

## 📘 Overview

Large-scale weather datasets often suffer from missing entries due to sensor failures or data transmission issues. This project explores deep learning-based methods for **temporal gap-filling**—reconstructing missing values in time series weather data. Using PyTorch, the model is trained to learn from corrupted and uncorrupted historical data to predict and restore the gaps in unseen sequences.

## 🧠 Problem Statement

Given daily weather data for a European city over a period of ~40 years, a portion of the data has been corrupted with missing entries. The training data includes three decades of corrupted datasets along with their original, uncorrupted versions. The final test set contains a fourth corrupted decade, for which the original values are no longer available.

The objective is to build a neural network that can infer and recover missing values in this test dataset, leveraging patterns learned from the historical data.

## 🗂️ Project Structure

- `Assessment.ipynb`: Contains all analysis, visualizations, model design, training loop, and final predictions.
- `test_set_nogaps.csv`: Output file with the reconstructed weather values for the test set.
- `References.md`: A record of all external tools and sources used during the project.
- `training_set/`: Folder containing input training data (`_nogaps.csv` and corrupted `.csv` files).
- `test_set.csv`: The corrupted test dataset to be reconstructed.

## 📊 Data Features

Each file includes daily records of:
- `date`
- `cloud_cover`
- `sunshine`
- `global_radiation`
- `max_temp`
- `mean_temp`
- `min_temp`
- `precipitation`
- `pressure`

## ⚙️ Methodology

1. **Exploratory Analysis**
   - Visualized trends and distributions before/after corruption.
   - Identified variable dependencies and patterns of missingness.

2. **Data Preparation**
   - Constructed paired datasets for supervised learning.
   - Implemented PyTorch `DataLoader`s for training and inference.

3. **Model Design**
   - Designed a temporal deep learning model using architectures such as LSTM, GRU, or Transformer variants.
   - Optimized using mean squared error (MSE) loss between corrupted inputs and their clean counterparts.

4. **Evaluation & Output**
   - Reconstructed the test dataset and visualized results.
   - Saved output in `test_set_nogaps.csv` maintaining original formatting.

## 🔬 Results

The trained model produced realistic reconstructions for missing weather values. Visual analysis confirmed consistency across features, and histograms showed that the imputed distributions closely aligned with the uncorrupted data.

## 📚 Skills & Tools

- Python, PyTorch
- Time Series Analysis
- Data Imputation
- Neural Network Architecture Design
- Data Visualization (Matplotlib, Seaborn)
- Git, GitHub

## 🏫 Academic Context

This project was submitted as part of a **24-hour individual coursework** for the **Deep Learning** module in the **MSc in Applied Computational Science and Engineering** at **Imperial College London**. It reflects a practical, time-constrained application of machine learning techniques to solve real-world data challenges.
