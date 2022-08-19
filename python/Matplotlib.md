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

Marker
```python
x = np.arrange(10)
fig, ax = plt.subplots()
ax.plot(x, x, marker=".")
ax.plot(x, x+2, marker="o")
ax.plot(x, x+4, marker="v") # triangle shape
ax.plot(x, x+6, marker="s") # square
ax.plot(x, x+8, marker="*")
```
![](https://user-images.githubusercontent.com/93812258/185700044-c7552994-fcf0-413d-a460-636ab3a24d2c.png)

Modifying
```python
x = np.linspace(0,10,1000) # start, end, step
fig,ax = plt.subplots()
ax.plot(x, np.sin(x)) # sin graph
ax.set_xlim(-2,12) # x axis limit (-2 to 12)
ax.set_ylim(-1.5, 1.5) # y axis limit (-1.5 to 1.5)
```
![](https://user-images.githubusercontent.com/93812258/185701466-8bccca00-0aab-44c0-9043-5b8687094f9b.png)

Legend
```python
x = np.arrange(10)
fig, ax = plt.subplots()
ax.plot(x, x, label='y=x')
ax.plot(x, x**2, label='y=x^2')
ax.set_xlabel("x")
ax.set_ylabel("y")
ax.legend(loc='upper right', shadow=True, fancybox=True, borderpad=2)
```
![](https://user-images.githubusercontent.com/93812258/185702409-35252d02-7ab6-44ba-bf3e-94cd3f093a6f.png)

