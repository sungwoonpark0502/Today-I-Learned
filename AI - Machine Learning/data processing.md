# Data Processing

* Most of the datas are in the form that cannot be used as a machine learning model. This is why we need to transform the data, which is called data processing
* Data Cleansing is also needed to eliminate unnecessary datas like non-sense datas and missing values
* Splitting Data is dividing data into training data and test data


## Processing Categorical Data

Data in the Red squares are the Categorical Data

![](https://user-images.githubusercontent.com/93812258/186034238-249cbb01-6ba7-4ead-a7c7-3ee7e23c6f38.png)

Ordinal Data: Red Square, if categoric size doesn't matter
Norminal Data: Blue Square, if categoric size matters

![](https://user-images.githubusercontent.com/93812258/186034581-b5e9deb5-7508-475c-b204-4fca335bb064.png)

### Data Processing for Ordinal Data
* Mapping Numbers (수치 맵핑 방식)
  * One example of this method is to change the category to numbers. Ex) Male = 1 and Female = 0
  ```python
  # using replace to change male to 1 and female to 0
  titanic = pd.read_csv('./data/titanic.csv')
  titanic = titanic.replace({'male': 0, 'female': 1})
  ```
* Dummy Method
  
  ```python
  titanic = pd.read_csv('./data/titanic.csv')
  dummies = pd.get_dummies(titanic[['Embarked']])
  ```
  
  * Example
  ![]()
  <img width="547" alt="Screen Shot 2022-08-23 at 8 17 52 AM" src="https://user-images.githubusercontent.com/93812258/186036058-45ab51f6-a816-4b65-97fc-5a3aceabee72.png">

### Data Processing for Norminal Data
* Mapping the Numbers (수치 맵핑 방식)
  * Examples and code written above

## Processing Numerical Data

Methods: Scaling(Normalization & Standardization) and Categorization

### Scaling Method
* Changing the size and range
* Use when there's a difference between the feature

1. Normalization

This Equation will change the datas to be between 0 ~ 1
![](https://user-images.githubusercontent.com/93812258/186038282-7176ab03-8199-4ecb-9b25-b74f6df30a1a.png)

```python
    data = (data-data.min())/(data.max()-data.min())
```

 2. Standardization
 
 This equation will chagne the datas' average to be 0 and standard deviation to 1
 
 ![](https://user-images.githubusercontent.com/93812258/186039239-f378d77c-1195-47c1-8900-221342df785d.png)
 
```python
data = (data-data.mean())/data.std()
```

3. 다변량 수치형 자료 변환하기
```python
data = (data-data.min(axis = 0))/(data.max(axis = 0)-data.min(axis = 0))
```

 ### Categorization
 * Used when category is more important than the variable value

Example: Predicting if the grade is above average. In this case, the grade itself is not important compared to whether it is above average or not.

![](https://user-images.githubusercontent.com/93812258/186039527-e4696dc2-b755-44f2-94aa-3867e3b98ca2.png)

## Data Cleansing
* Eliminating Missing Data(Null, None, Nan, etc)
  * Ways to do this:
    * Deleting the sample that the missing data is in
    * Deleting the variable that has numerous missing data
    * Exchanging the missing data to other value
    
```python
# Eliminating Missing Data
titanic_1 = titanic.drop(columns=['Cabin']) # deletes Cabin variable

titanic_2 = titanic_1.dropna() # deletes the sample that contains missing data

```

* Eliminating Outlier
  * Outlier can reduce the model's performance
```python
titanic_3 = titanic_2[titanic_2['Age']-np.floor(titanic_2['Age']) == 0 ]
```

## Splitting Data
* Splitting the data to training data and test data
* Usually 7:3 ~ 8:2 = training data : test data
* Splitting Supervised Learning Data into:
  * Feature Data: to predict the label
  * Label Data: data that's targeted to be predicted
  
  Predicting the number of survivers:
  ![](https://user-images.githubusercontent.com/93812258/186041115-0177f8e9-e2b3-4ec5-974f-14d12c0d2562.png)

```python
# splitting feature data and label data
X = titanic_3.drop(columns=['Survived'])
y = titanic_3['Survived']

# Splitting the X and y data into training and test data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)
```
