---
tag: python, computing, programming, computacao, listas, inteiros, boasPraticas
---
# Listas x Inteiros

``` python
def foo(x): 
	x[0] = 99
my_list = [1, 2, 3]
foo(my_list)
print(my_list)
```
Output:
	[99, 2, 3]

```py
def bar(x):
	x = x + 90
my_var = 3
bar(my_var)
print(my_var)
```
Output:
	3
	
	