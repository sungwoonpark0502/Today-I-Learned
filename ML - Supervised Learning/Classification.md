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

![](https://user-images.githubusercontent.com/93812258/187019092-ca6ed2fa-c12a-4157-aa90-b6b501103272.png )
