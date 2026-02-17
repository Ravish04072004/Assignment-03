# Assignment 3: Probability Density Function Estimation

**Name:** Ravish Sharma  
**Roll Number:** 102303651

## Project Description

This project implements a solution to estimate the parameters of a Probability Density Function (PDF) after transforming a feature, `no2`, using a non-linear model parameterized by the roll number.

### Transformation Function
The feature $x$ (from column `no2`) is transformed into $z$ using:
$$ z = T_r(x) = x + a_r \sin(b_r x) $$

Where parameters $a_r$ and $b_r$ are derived from the roll number **102303651**:
- $a_r = 0.05 \times (102303651 \pmod 7) = 0.1$
- $b_r = 0.3 \times (102303651 \pmod 5 + 1) = 0.6$

### Parameter Estimation
The transformed data $z$ is fitted to the target PDF:
$$ \hat{p}(z) = c \cdot e^{-\lambda(z-\mu)^2} $$

The estimated parameters are:
- **c** $\approx$ 0.0315
- **$\lambda$** $\approx$ 0.0034
- **$\mu$** $\approx$ 19.85

## Files in Repository
- `assignment03.ipynb`: Jupyter Notebook containing the code for data loading, transformation, visualization, and parameter estimation.
- `data.csv`: Source dataset containing air quality data (specifically the `no2` column).
- `README.md`: This file.

## Requirements
To run this notebook, you need the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `scipy`

## How to Run
1. Ensure `data.csv` is in the same directory (or `data.csv (1)/data.csv`).
2. Open `assignment03.ipynb` in Jupyter Notebook or JupyterLab.
3. Run all cells to see the original vs. transformed histograms and the fitted PDF curve.
