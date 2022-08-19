# Matplotlib

## Matplotlib Graph

### Line Plot
```python
fig, ax = plt.subplots() # if empty, generates 1 figure
x = np.arange(15) # 0~14
y = x ** 2 # equal to y = x^2
ax.plot(
x, y,
linestyle=":", # connected by dots
marker="*", # points illustrated as *
color="#524FA1"
)
```
![a](https://user-images.githubusercontent.com/93812258/185698421-4ceff53c-053d-4892-953e-025d25b96e7e.png)

Line Style
```python
x = np.arrange(10) # 1~9
fig, ax = plt.subplots()
ax.plot(x ,x,linestyle="-") # solid, 4th one(bottom)
ax.plot(x ,x+2,linestyle="--") # dashed, 3rd one
ax.plot(x ,x+4,linestyle="-.") # dashdot, 2nd one
ax.plot(x ,x+6,linestyle=":") # dotted, 1st one(top)
```
![](https://user-images.githubusercontent.com/93812258/185699149-4b741d4f-992c-4f3a-87e7-4e31bb7d8c9c.png)

Color
```python
x = np.arrange(10)
fig, ax = plt.subplots()
ax.plot(x, x, color="r")
ax.plot(x, x+2, color="green")
ax.plot(x, x+4, color="0.8")
ax.plot(x, x+6, color="#52FA1")
```
![](https://user-images.githubusercontent.com/93812258/185699572-442512d3-53b3-47a3-b40b-98a8a299974e.png)
