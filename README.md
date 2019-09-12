#
# Linear Regression 

This repository contains a commented Python Jupyter Notebook with basic Ordinary Least Squares Linear Regression implementation

https://github.com/jorgesleonel/linear-regression/blob/master/Boston%2BHousing%2BPricing%2BLinear%2BRegression.ipynb


Linear regression is a statistical method of finding the relationship between independent and dependent variables.

For example: associating years of professional experience with remuneration.

In this case, “Years of Experience” is an independent variable (ie., we cannot mathematically determine the years of experience) and “Compensation” is a dependent variable (goal is to determine / predict salary — the dependent variable — based on years of experience).

# Fitting the best intercept line

“Sum of Squared Errors” (SSE) is a simple, straightforward method to fit intercept lines between points — and compare those lines to find out the best fit through error reduction. The errors are the sum difference between actual value and predicted value.

# The role of OLS -Ordinary Least Squares

Next, the “Ordinary Least Squares” (OLS) method is used to find the best line intercept (b) and the slope (m). [in y = mx + b, m is the slope and b the intercept]

With OLS Linear Regression the goal is to find the line (or hyperplane) that minimizes the vertical offsets. We define the best-fitting line as the line that minimizes the sum of squared errors (SSE) or mean squared error (MSE) between our target variable (y) and our predicted output over all samples i in our dataset of size n.

It is important to point out though that OLS method will work for a univariate dataset (ie., single independent variables and single dependent variables). Multivariate dataset contains a single independent variables set and multiple dependent variables sets, requiring a machine learning algorithm called “Gradient Descent”.

# Gradient Descent Algorithm (GDA)

GDA’s main objective is to minimise the cost function.
Cost function h𝜽 helps us to figure out the best possible values for 𝜽0 and 𝜽1 which would provide the best fit line for the data points.

It is one of the best optimisation algorithms to minimise errors (difference of actual value and predicted value). Using GDA we will figure out a minimal cost function by applying various parameters for 𝜽0 and 𝜽1 and see the slope intercept until it reaches convergence.

In other words → we start with some values for 𝜽0 and 𝜽1 and change these values iteratively to reduce the cost. Gradient descent helps us on how to change the values.

It works roughly like this:

* take a step towards downward direction;
* from the each step, look out the direction again to get down faster and downhill quickly.

Mathematically speaking:

1. To update 𝜽0 and 𝜽1 we take gradients from the cost function. To find these gradients, we take partial derivatives with respect to 𝜽0 and 𝜽1
The partial derivatives are the gradients and they are used to update the values of 𝜽0 and 𝜽1 .
2. The number of steps taken is the learning rate (𝛼 below). This decides on how fast the algorithm converges to the minima.
Alpha is the learning rate which is a hyperparameter that you must specify. A smaller learning rate could get you closer to the minima but takes more time to reach the minima. A larger learning rate converges sooner but there is a chance that you could overshoot the minima.

[!Regression](http://rasbt.github.io/mlxtend/user_guide/regressor/LinearRegression_files/simple_regression.png)

