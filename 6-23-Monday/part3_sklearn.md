# Monday, 6/23/25

## Part 3: Machine Learning with sklearn

### Code from class

```
from sklearn import linear_model, model_selection, metrics

reg = linear_model.LinearRegression().fit(salaries[["YearsExperience"]],salaries[["Salary"]])

print(reg.coef_)
print(reg.intercept_)

X_train, X_test, y_train, y_test = model_selection.train_test_split(salaries[["YearsExperience"]], salaries[["Salary"]], test_size = 0.2, random_state=1234)
   
reg = LinearRegression().fit(X_train, y_train)
y_pred = reg.predict(X_test)
   
metrics.r2_score(y_test, y_pred)
metrics.mean_squared_error(y_test, y_pred)

reg.score(X_test, y_test)

```
X_train, X_test, y_train, y_test = model_selection.train_test_split(aq[["CO", "NMHC", "NOx"]], aq[[“O3”]], test_size = 0.2, random_state=123)

reg = linear_model.LinearRegression().fit(X_train, y_train)

reg.score(X_test, y_test)

pd.DataFrame({"column" : X_test.columns, "coefficient" : reg.coef_}).sort_values("coefficient")
```

1. For the "scores" dataset, "Average Score (SAT Writing)" will be the dependent variable. Choose a column to use as the predictor variable (independent variable).
1. Split the data into a training and testing set (what fraction of the data will you use for testing?).
1. Train a linear model using the training data.
1. “Predict” the dependent variable based on the independent variable using the test set. Use `metrics.r2_score()` and  `metrics.mean_squared_error()` to evaluate the prediction.
1. Try a few different random seeds for the train/test split. How different are your answers?
1. Try training your model based on all of the data rows, rather than splitting it into train/test. How do the metrics compare?
1.  Try different possible independent variables for the model. Which variable provides the most accurate predictions?
1. Try training a linear regression model on all of the quantitative variables from the SAT scores dataset (remember to split into train and test set).
1. Find the score of this model. How does it compare to the score of models trained on a single variable?
1. Download the apple quality dataset: https://drive.google.com/file/d/1MJGf7XJSdrGCy6hKDtvS9rt5HvlevMK6/view?usp=sharing. Decide on a column to use as the dependent variable. Try predicting the dependent variable based on the independent variables. Which independent variables are most useful for predicting the dependent variable?

