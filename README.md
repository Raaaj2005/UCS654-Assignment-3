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

1. DependenciesThis project requires Python and the following libraries: pandas: For data manipulation. numpy: For numerical operations and transformations. scipy: For curve fitting (optimization). To install them, run: Bashpip install pandas numpy scipy
2. DatasetThe project uses the India Air Quality Data (city_day.csv). Source: Kaggle - India Air Quality DataEnsure the file is placed in the root directory or update the path in assignment_solver.py. Usage: Clone the repository: Bashgit clone [https://github.com/Raaaj2005/Assignment-3-Advanced-Mathematics.git](https://github.com/Raaaj2005/Assignment-3-Advanced-Mathematics.git)
Navigate to the project folder. Run the solver script: Bashpython assignment_solver.py

## Results & Output

The script calculates and outputs the optimal parameters required for submission:
* **Lambda ($\lambda$)**
* **Mu ($\mu$)**
* **c**

## Author
* **Name:** Raj
* **Roll Number:** 102317090
* **University:** Thapar Institute of Engineering and Technology
