

---
tag: python, computing, programming, computacao, contextManager, functions, função, boasPraticas
---
# Context Manager

Context manager são funções que:
- Criam um contexto 
- Rodam o código 
- Removem o contexto

# Exemplo
```py
with open('file.txt') as file:
	text = file.read()
	length = len(text)
print(f'O arquivo tem o tamanho de {length} caracteres')
```

O _open()_ faz 3 coisas: 
- Cria um contexto abrindo um arquivo
- Permite rodar qualquer código dentro daquele arquivo
- Remove o contexto fechando aquele arquivo

# Aplicações
Um context manager permite, por exemplo, executar um código que precisa ser executado em nível de administrador e retornar ao nível de usuário comum logo após a execução:

```python
with admin_user(req):
	#do some special logic
	#as an admin user
#back to regular stuff
	
```

[^1] Source: https://www.youtube.com/watch?v=cSbD5SKwak0&t=795s