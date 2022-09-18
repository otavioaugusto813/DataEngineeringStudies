---
tag: python, computing, programming, computacao, doOneThing, otimizacao, boasPraticas
---
# Do One Thing

O código abaixo viola um dos princípios do Desenvolvimento de Software. Ele faz muitas coisas: 
- Carrega o dado
- Plota o dado
- Retorna o dado carregado
![](../../../Anexos/Pasted%20image%2020220915233326.png)
Deve-se seguir o princípio do "Do One Thing". 

Podemos dividir a função em mais de uma:
O código se torna mais flexível, já que cada parte pode ser utilizada em diferentes contextos.
![](../../../Anexos/Pasted%20image%2020220915233542.png)
## Vantagens de fazer uma coisa apenas

O código se torna: 
- Mais flexível
- Mais compreensível
- Mais fácil de testar
- Mais fácil de debugar
- Mais fácil de alterar
