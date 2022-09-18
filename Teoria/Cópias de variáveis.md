

---
tag: python, computing, programming, computacao
---
# Cópias de variáveis

``` python
a = [1, 2, 3]
b = a
a.append(4)
print(b)
```
Output:
	[1,2,3,4]

Percebe-se que a lista b também recebeu o novo valor quando se fez um append em a. Isso acontece porque b aponta para a, uma alteração em a também altera b.
![](../../../Anexos/Pasted%20image%2020220916172441.png)

O mesmo ocorre ao contrário
``` py
b.append(5)
print(a)
```
Output: 
	[1,2,3,4,5]

Se alterarmos a variável a (reatribuir) , contudo, b deixará de apontar para ela.

```py
a = 42
```

![](../../../Anexos/Pasted%20image%2020220916172905.png)
