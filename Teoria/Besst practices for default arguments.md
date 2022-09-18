---
tag: python, computing, programming, computacao, boasPraticas, funcoes
---
# Best practices for default arguments
Usar variáveis mutáveis como argumentos padrão para uma função pode gerar problemas no código, visto que elas podem ser alteradas sem controle ou fora da função.
Nestes casos, o ideal é verificar se a variável é nula (None) e só assim alterá-la 

``` python
def foo(var = None):
	if var is None:
		var = []
	var.append(1)
	return var
```