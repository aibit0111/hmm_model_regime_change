# hmm_model_regime_change

# Regime Detection in Bitcoin Using Hidden Markov Models (HMM) and Alpha-Stable Distributions

## Overview
This repository demonstrates how to detect regime changes in financial markets, specifically Bitcoin, using **Hidden Markov Models (HMM)** with non-Gaussian **Alpha-Stable distributions**. The project uses the **pomegranate** library, which supports non-Gaussian distributions like Alpha-Stable, making it ideal for modeling Bitcoin’s highly volatile and non-normal return distribution.

### Key Concepts:
- **Hidden Markov Models (HMM)**: A statistical model where the system being modeled is assumed to follow a Markov process with hidden states.
- **Alpha-Stable Distributions**: Flexible distributions capable of modeling fat tails and asymmetry in financial data, unlike Gaussian distributions.
- **Regime Detection**: The identification of different market conditions (e.g., bull, bear, and range markets) and their transitions over time.

## Features
- **Simulated Bitcoin Data**: Simulates market conditions with bull, bear, and range markets, each with varying volatility levels.
- **Alpha-Stable HMM**: Uses Hidden Markov Models with Alpha-Stable distributions to model the returns.
- **Regime Prediction**: Detects market regimes based on the modeled data.
- **Visualization**: Visualizes the identified regimes on the time series data.
- **CSV Export**: Exports the time series and corresponding regimes to a CSV file for further analysis.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/regime-detection-bitcoin-hmm.git
    ```

2. **Navigate to the project directory**:
    ```bash
    cd regime-detection-bitcoin-hmm
    ```

3. **Install the required dependencies**:
    This project uses the following libraries:
    - `pomegranate` for HMM modeling
    - `numpy`, `pandas` for data manipulation
    - `matplotlib` for visualization

    Install them using the following command:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Step 1: Simulate Data
Run the notebook `hmm_regime_detection.ipynb`, which simulates Bitcoin-like returns for 6 different market regimes (bull/bear/range with low/high volatility).

### Step 2: Fit Hidden Markov Model
The notebook fits a Hidden Markov Model using **pomegranate** with **Alpha-Stable distributions**, making it ideal for modeling Bitcoin’s returns. It detects the underlying regimes in the simulated time series data.

### Step 3: Predict and Visualize Regimes
The predicted regimes are visualized alongside the simulated returns, with each regime (market condition) highlighted using different colors.

### Step 4: Export Results
The results (time series with predicted regimes) are exported as a CSV file for further analysis.

### Example Notebook:
The core logic is implemented in the Jupyter notebook `hmm_regime_detection.ipynb`. Here’s a brief breakdown:
- Simulates market regimes using **numpy**.
- Trains an HMM with **pomegranate** using **Alpha-Stable distributions**.
- Predicts the hidden states (regimes) and visualizes them using **matplotlib**.
- Exports the results to `regimes_prediction.csv`.

## File Structure

