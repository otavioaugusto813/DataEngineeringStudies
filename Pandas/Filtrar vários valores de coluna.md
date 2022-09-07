## Filtrar vários valores de coluna

```python

pregoes = pregoes[pregoes['LICITAÇÃO'].str.contains("/2019|/2020|/2021")]