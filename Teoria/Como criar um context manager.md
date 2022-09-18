---
tag: python, computing, programming, computacao, contextManager
---
# Como criar um [Context Manager](Context%20Manager.md)

- Defina uma função
- (Opcional) Adicione algum código para configurar seu código
- Use o *yield* keyowrd.
- Adicione `@contextlib.contextmanager` decorator
## Implementação
``` python
@contextlib.contextmanager 
def my_context():
	print('hello')
	yield 42
	print('goodbye')
```
## Execução
``` python
with my_context() as foo:
	print(f'foo is {foo}')
```
## Output
`hello
`foo is 42
`goodbye`

