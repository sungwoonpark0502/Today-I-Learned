![](https://user-images.githubusercontent.com/93812258/187018918-339f3631-e09a-4537-9b8a-9b76687aa1e0.png)

```python
# 풍속에 따른 항공 지연 여부 데이터
Wind = [1, 1.5, 2.5, 5, 5.5, 6.5]
Delay  = ['No', 'No', 'No', 'Yes', 'Yes', 'Yes']

# 위 데이터를 DataFrame 형태로 저장합니다.
data = pd.DataFrame({'풍속': Wind, '지연 여부': Delay})
print(data,'\n')

"""
1. binary_tree 모델을 사용하여 항공 지연 여부를 예측합니다.
"""
data_pred = binary_tree(data, threshold = 4)

"""
1. 학습용 평가용 데이터로 분리합니다
"""
train_X, test_X, train_Y, test_Y = train_test_split(X, Y, test_size=0.2, random_state = 42)

"""
1. test_X에 대해서 예측합니다.
"""
pred_X = DTmodel.predict(test_X)
```

## Confusion Matrix
![](https://user-images.githubusercontent.com/93812258/187019054-f08c3642-f6db-4fc2-96d0-f0601c05f35c.png)

![](https://user-images.githubusercontent.com/93812258/187019092-ca6ed2fa-c12a-4157-aa90-b6b501103272.png)

![](https://user-images.githubusercontent.com/93812258/187019309-b116093f-f4b7-4f34-ba7a-3ee8762a328b.png)

```python
"""
1. 혼동 행렬을 계산합니다
"""
cm = confusion_matrix(test_Y, y_pred) # confusion_matrix() 를 활용하여 혼동행렬을 계산합니다.

"""
1. 정확도를 계산합니다.
"""
acc_train = DTmodel.score(train_X, train_Y) # score() 함수를 활용하여 정확도를 계산합니다.
acc_test = DTmodel.score(test_X, test_Y)

"""
1. 정밀도를 계산합니다.
"""
precision_train = precision_score(train_Y, y_pred_train) # precision_score()를 활용하여 정밀도를 계산합니다.
precision_test = precision_score(test_Y, y_pred_test)

"""
2. 재현율을 계산합니다.
"""
recall_train = recall_score(train_Y, y_pred_train) # recall_score()를 활용하여 재현율을 계산합니다.
recall_test = recall_score(test_Y, y_pred_test)
```
