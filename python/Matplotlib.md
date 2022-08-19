# Matplotlib

## Matplotlib Graph

### Line Plot
```python
fig, ax = plt.subplots()
x = np.arange(15)
y = x ** 2
ax.plot(
x, y,
linestyle=": ",
marker="*",
color="#524FA1"
)
```
![a](https://user-images.githubusercontent.com/93812258/185698421-4ceff53c-053d-4892-953e-025d25b96e7e.png)

