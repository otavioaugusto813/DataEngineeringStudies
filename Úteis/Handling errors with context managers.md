---
tag: python, computing, programming, computacao
---
# Handling errors with context managers

``` python
def get_printer(ip):
	p = connect_to_printer(ip)

	try:
		yield
	finally:
		p.disconnect()
		print('Desconectado da impressora')
doc = {"text": "Este é o meu texto"}
with get_printer('10.0.34.111') as printer:
	printer.print_page(doc['txt'])
```

## Resultado
![](../../../Anexos/Pasted%20image%2020220917190525.png)