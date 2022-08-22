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

