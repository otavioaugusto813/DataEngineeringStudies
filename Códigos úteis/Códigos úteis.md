# Python

# Códigos úteis

## Corrigir valores de moeda de acordo com os tipos mistos encontrados na coluna de tipo "object"

```python

df['Valor'] = df['Valor'].apply(lambda x: x.replace('$', '').replace(',', '')
if isinstance(x, str)else x).astype(float)
```

## Corrigir múltiplos valores de uma mesma coluna com um dicionário

```python

entrega_distribuicao.replace({'PROCESSO DE COMPRA': correcao}, regex = True)
```

## Filtrar vários valores de coluna

```python

pregoes = pregoes[pregoes['LICITAÇÃO'].str.contains("/2019|/2020|/2021")]
```

## Tirando os acentos das palavras

```python
COLUNA.str.normalize('NFKD').str.encode('ascii', errors='ignore').str.decode('utf-8')  
```

## Trocando valores de uma coluna

```python
COLUNA.replace('value1', 'value2', regex = True)
```

## Corrigindo vários valores de uma mesma coluna

```python
correcao = {'\\*\\*\\*' : np.nan, "-":np.nan }      # corrigindo valores de nota de empenho                                                                                    

entrega_distribuicao = entrega_distribuicao.replace({'NOTA DE EMPENHO': correcao}, regex = True)

entrega_distribuicao['NOTA DE EMPENHO'] = entrega_distribuicao['NOTA DE EMPENHO'].astype('float')
```

## Criando uma nova coluna condicional com np.select()

```python
condicoes = [(df['lead_time'] < 50), 
            ((df['lead_time'] > 50) & (df['lead_time'] < df['lead_time'].mean()))]

escolhas = ['baixo', 'medio']

coluna_aux = np.select(condicoes, escolhas, default = 'alto')
```

[Remover pontuação](Remover%20pontuação.md)```
[Limpar texto](Limpar%20texto.md)
```

## Parse dates no Pandas

```python
from datetime import datetime
def parser(x):
    return datetime.strptime('190'+x, '%Y-%m')
```

## [Definir classe abstrata](https://www.python-course.eu/python3_abstract_classes.php)

[Definir classe abstrata](Definir%20classe%20abstrata.md)

## Transformando nested lists em flat lists

```python
from functools import reduce
lista = reduce (lambda x, y: x + y, lista)
```

# Artigos

[Cleaning Up Currency Data with Pandas - Practical Business Python](https://www.notion.so/Cleaning-Up-Currency-Data-with-Pandas-Practical-Business-Python-616f6fd30eaf447fbc4885d668996ba8)

[Úteis](https://www.notion.so/teis-d20f86570ada46bb823b10889a3c8b37)