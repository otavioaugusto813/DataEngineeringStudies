## Transformando nested lists em flat lists

```python
from functools import reduce
lista = reduce (lambda x, y: x + y, lista)