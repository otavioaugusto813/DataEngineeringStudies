---
tag: python, computing, programming, computacao, scope, teoria
---

# Scope

O scope determina quais variáveis podem ser acessadas em diferentes pontos do código.

## Regras para determinar o escopo
1. Primeiro o interpretador procura dentro do escopo *local* 
2. Depois, procura no contexto *global* 

No exemplo abaixo, pode-se ver que a variável x só se torna visível fora da função se a definirmos como global. Contudo, deve-se evitar tal declaração como global, já que torna mais difícil debugar o código e o torna mais exposto a camadas externas.

![](../../../Anexos/Pasted%20image%2020220918190649.png)
## [[../Úteis/Nonlocal keyword]] 

Se quisermos utilizar uma variável que pertence a uma função pai, podemos utilizar o nonlocal keyword.