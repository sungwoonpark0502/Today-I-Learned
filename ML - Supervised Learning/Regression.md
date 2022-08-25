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
![](https://user-images.githubusercontent.com/93812258/186107646-f124c2f9-1fcd-468f-b7cf-c3eae5c0b9f2.png)

```python
"""
1. Sales 변수는 label 데이터로 Y에 저장하고 나머진 X에 저장합니다.
"""
X = df.drop(columns=['Sales'])
Y = df['Sales']

"""
2. 2:8 비율로 (test_size = 0.2) X와 Y를 학습용과 평가용 데이터로 분리합니다.
"""
train_X, test_X, train_Y, test_Y = train_test_split(X, Y, test_size=0.2, random_state=42) 

"""
1.  다중 선형 회귀 모델을 초기화 하고 학습합니다
"""
lrmodel = LinearRegression() # LinearRegression 모델을 초기화 합니다.
lrmodel.fit(train_X, train_Y) # train_X와 train_Y 데이터로 모델을 학습합니다.

"""
2. 학습된 파라미터 값을 불러옵니다
"""
beta_0 = lrmodel.intercept_ # y절편 (기본 판매량)
beta_1 = lrmodel.coef_[0] # 1번째 변수에 대한 계수 (페이스북)
beta_2 = lrmodel.coef_[1] # 2번째 변수에 대한 계수 (TV)
beta_3 = lrmodel.coef_[2] # 3번째 변수에 대한 계수 (신문)

"""
1. test_X에 대해서 예측합니다.
"""
pred_X = lrmodel.predict(test_X) # predict()를 활용해서 예측합니다.

"""
2. df1에 대해서 예측합니다.
"""
pred_df1 = lrmodel.predict(df1) # predict()를 활용해서 예측합니다.
```

# Evaluating Linear Regression
* Ex) RSS, MSE, MAE, MAPE, R^2

RSS

![](https://user-images.githubusercontent.com/93812258/186613166-bb197707-9916-4940-8a34-dda8d1dd087d.png)

```python
"""
1. train_X 의 RSS 값을 계산합니다
"""
RSS_train = np.sum( (train_Y - pred_train) ** 2) # 예측값과 실제값의 오차제곱합을 구합니다.
```

MSE
![](https://user-images.githubusercontent.com/93812258/186614186-07980026-e240-4cde-97af-0becf014d31c.png)

```python
"""
1. train_X 의 MSE 값을 계산합니다
"""
MSE_train = mean_squared_error(train_Y, pred_train) # mean_squared_error() 를 활용해서 MSE를 계산합니다.
```

MAE
![](https://user-images.githubusercontent.com/93812258/186614371-64ff017c-0c26-4047-a5f1-f33907b82820.png)

```python
"""
1. train_X 의 MAE 값을 계산합니다
"""
MAE_train = mean_absolute_error(train_Y, pred_train) # mean_absolute_error() 를 활용해서 MAE를 계산합니다.
```

R2
* Lower the R^2, worser the model is

![](https://user-images.githubusercontent.com/93812258/186615231-95543369-1373-46fb-8766-a4f08194cd42.png)

```python
"""
1. train_X 의 R2 값을 계산합니다
"""
R2_train = r2_score(train_Y, pred_train) # r2_score()를 활용하여 R2값을 계산합니다.

"""
2. test_X 의 R2 값을 계산합니다
"""
R2_test = r2_score(test_Y, pred_test) # r2_score()를 활용하여 R2값을 계산합니다.
```
