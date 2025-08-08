# AI-Stock-Market-Trend-Prediction
This project implements a Generative Adversarial Network (GAN) to forecast short-term stock market trends using historical price data. The Generator model creates plausible future price sequences based on past data, while the Discriminator evaluates their authenticity against real market data.
## 🚀 Features
- **Data Preparation Pipeline** for creating time-step sequences from historical stock data.
- **GAN Architecture**: Generator (Dense + LeakyReLU + BatchNorm) and Discriminator (Dense + Sigmoid).
- **Prediction Horizon**: 60 future time steps.
- Built with **Keras & TensorFlow** for deep learning.
- Flexible to adapt for any stock dataset.
- Planned **Power BI Integration** for real-time visualization.

---

## 📂 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Future Improvements](#future-imporvements).

## 📜 Overview
Stock market prediction is a complex task due to volatility and numerous influencing factors.  
This project uses **Generative AI** to model price sequences and forecast likely short-term movements.  
By training on historical OHLC (Open, High, Low, Close) data, the model learns temporal patterns and generates realistic predictions.

---

## 📊 Dataset
- **Source:** [Kaggle - stock_data](https://www.kaggle.com/)  
- Features: Open, High, Low, Close, Volume.
- Time frame: User-defined (can adapt to different periods).
- Preprocessing:
  - Scaling data between 0 and 1.
  - Creating sequences with `time_step=60` for training.
---
## 🧠 Model Architecture

### Generator
- Input: Random noise vector.
- Layers: Dense → LeakyReLU → BatchNorm (repeated) → Dense (time_step) → Reshape.
- Output: Predicted sequence of stock prices.

### Discriminator
- Input: Real or generated sequences.
- Layers: Flatten → Dense → LeakyReLU → Dense (1) with Sigmoid activation.
- Output: Probability of sequence being real.

**Loss Function:** Binary Crossentropy  
**Optimizer:** Adam

## ⚙️ Installation
```bash
# Clone the repository
git clone https://github.com/YourGitHubUsername/AI-Stock-Market-Trend-Prediction.git
cd AI-Stock-Market-Trend-Prediction

# Install dependencies
pip install -r requirements.txt

## Usage

# Open the .ipynb notebook in Google Colab.
# Upload your dataset from Kaggle or connect via the Kaggle API.
# Run all cells to train and evaluate the model.

## Results

# Generator produces realistic price trend sequences.
# Example graph of actual vs generated prices.
# Loss curves for both Generator & Discriminator.

## Future Improve Movements

### Model Accuracy Enhancement
# Experiment with different time-step sizes and sequence lengths to better capture market patterns.

### Data Improvements
# Use higher-quality datasets with minute-level or tick-level data for more granular predictions.

### Interactive Dashboard → Create with Power BI, Tableau, or Streamlit to visualize:
# Actual vs Predicted trends
# Prediction error over time
# Volatility maps
