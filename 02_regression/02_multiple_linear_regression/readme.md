# Multiple linear regression 👨‍🔬

- An extension of the simple linear regression model.

- It is a statistical method that allows us to predict the value of a variable based on the value of two or more other variables.

---

## Dummy variable trap: 🤜

- When we have a categorical variable with more than two categories, we need to create dummy variables for each category.
- We need to drop one of the dummy variables to avoid the dummy variable trap.

**For example**: If we three states, Bihar, UP and MP, we need to create three dummy variables, one for each state. But, if a person doesn't belongs to either UP or MP, then we can for sure state that he belongs to Bihar. So, we can drop the Bihar dummy variable.

### But, why do we need to drop one of the dummy variables?
-> It is because, we also have a constant term in our multiple linear regression equation. And, one of the field (lets say X1, essentially means X1 = 1 - X2 - X3). That is, if a person is not a member of UP or MP, then he is a member of Bihar. So, we can drop the Bihar dummy variable. 

- One question that might arise is, UP and MP are getting representation, but Bihar is not. Won't it harm the learning factor (coefficent) for Bihar. **No**, it won't. Because, the constant term will take care of that.

---

## How to build models for the multiple linear regression?

- The most important thing to remember is: **Garbage in, garbage out**. So, we need to make sure that we only take the features that are highly correlated with the dependent variable.

- So, we might need to drop many features, and that is totally fine.

- We can use the [**backward elimination**](https://www.youtube.com/watch?v=ZSYYLRPrEaY) method to build our model.

- We can also use the **all-in** method, where we take all the features and then remove the features that are not statistically significant.

---

## Coding multiple linear regression in Python using scikit-learn:

- All the steps are same as the simple linear regression.

- We won't need to do any feature scaling, because the library takes care of that.

- We also don't need to do anything for the dummy variable trap, because the library takes care of that too.

- And for the backward elimination part, we again don't need to do anything. Sci-kit learn has a class called [**LinearRegression**](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html) which takes care of all the things.

```python
from sklearn.linear_model import LinearRegression
regressor = LinearRegression()

regressor.fit(X_train, y_train)
y_pred = regressor.predict(X_test)
```

- We can't draw graph here, as it is not a 2D problem. There're multiple features (more than 1 independent variable), so we can't draw a graph.

```python
# concatenate the predicted and actual values, and then compare them
np.set_printoptions(precision=2)
print(np.concatenate((y_pred.reshape(len(y_pred),1), y_test.reshape(len(y_test),1)),1))
```

---

``` python
# to get the intercept
print(regressor.intercept_)

# for retrieving the slope:
print(regressor.coef_)

# predict for a single value
print(regressor.predict([[1, 0, 0, 160000, 130000, 300000]]))
```
