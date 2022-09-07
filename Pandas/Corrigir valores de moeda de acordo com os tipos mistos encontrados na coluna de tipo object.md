## Corrigir valores de moeda de acordo com os tipos mistos encontrados na coluna de tipo "object"

```python

df['Valor'] = df['Valor'].apply(lambda x: x.replace('$', '').replace(',', '')
if isinstance(x, str)else x).astype(float)
