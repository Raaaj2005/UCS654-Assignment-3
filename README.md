# Assignment 3: PDF Estimation with Non-Linear Model

## Project Overview
This project performs statistical analysis and parameter estimation on India's Air Quality data. The objective is to transform the `NO2` feature using a unique non-linear model derived from a university roll number and then fit a probability density function (PDF) to the transformed data using optimization techniques.

## Mathematical Model

### 1. Data Transformation
The feature $x$ (NO2 levels) is transformed into a new variable $z$ using the following roll-number parameterized equation:

$$z = x + a_r \sin(b_r x)$$

**Parameters for Roll Number `102317090`:**
* **$a_r$**: $0.05$
* **$b_r$**: $0.3$

### 2. Probability Density Function (PDF)
We fit the transformed data $z$ to the following function:

$$\hat{p}(z) = c \cdot e^{-\lambda(z-\mu)^{2}}$$

Where:
* $\mu$ (Mu): Mean of the distribution.
* $\lambda$ (Lambda): Variance scaling factor.
* $c$: Amplitude/Normalization constant.

## Project Structure

Setup & Prerequisites

1. Dependencies - This project requires Python and the following libraries:
   pandas: For data manipulation.
   numpy: For numerical operations and transformations.
   scipy: For curve fitting (optimization).
2. Dataset - The project uses the India Air Quality Data (data.csv). Source: Kaggle - India Air Quality Data

## Results & Output

The script calculates and outputs the optimal parameters required for submission:
* **Lambda ($\lambda$)** : 0.0033501700806893874
* **Mu ($\mu$)** 
* **c**

## Author
* **Name:** Raj
* **Roll Number:** 102317090
* **University:** Thapar Institute of Engineering and Technology
