# Simple linear regression💹

Simple Linear Regression is a type of Regression algorithms that models the relationship between a dependent variable and a single independent variable. The relationship shown by a Simple Linear Regression model is linear or a sloped straight line, hence it is called Simple Linear Regression.

### The equation of a straight line is:``` y = mx + c```.

## To use this model, we need to follow the following steps:
 
- Import the ```LinearRegression``` class from the ```sklearn.linear_model``` module.
- Create an instance of the ```LinearRegression``` class.
- Fit the model to the training data.
- Predict the response for the test data.

```python
from sklearn.linear_model import LinearRegression
regressor = LinearRegression()

# fit the regressor with X and Y data
regressor.fit(X_train, y_train)

# Predicting the Test set results
y_pred = regressor.predict(X_test)

# to get the intercept
print(regressor.intercept_)

# for retrieving the slope:
print(regressor.coef_)

# predict for a single value
print(regressor.predict([[5]])) # we're passing in the value as a 2D array
```