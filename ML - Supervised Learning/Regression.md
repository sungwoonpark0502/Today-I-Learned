# Regression

* An algorithm by finding the best model that explains the data and predicts the future data
* Loss Function: method of evaluating how well your algorithm models your dataset
    * Lower the function value, the better model
    * Gradient Descent
 1. Initialize Random (b0,b1)
 2. Calculate Loss
 3. Caluclate Gradient
 4. Update b0, b1

### Simple Linear Regression

 ![](https://user-images.githubusercontent.com/93812258/186100723-d0abda25-8451-4a83-95e9-d961af7baf74.png)

![](https://user-images.githubusercontent.com/93812258/186101224-45be060f-0893-4a9e-abd0-0483f3b0ed10.png)

```python
# Changing the column 'X' of X to DataFrame
train_X = pd.DataFrame(X, columns=['X'])

# Changing Y to Series
train_Y = pd.Series(Y)

# Initializing the Model. In this case,  LinearRegression
lrmodel = LinearRegression()

# Learning the data from train_X and train_Y
lrmodel.fit(train_X, train_Y)

# Predicting train_X
pred_X = lrmodel.predict(train_X)
```

### Multiple Linear Regression
* Used when we are trying to predict Y with many input data X1
