---
tag: python, computing, programming, computacao, nonLocal, kwyword
---
# Nonlocal keyword

``` python
def foo():
	x = 10
	def bar():
		nonlocal x
		x = 2000
		print(x)
	bar()
	print(x)

```

```python
foo()
```
## Output
```
200
200
```