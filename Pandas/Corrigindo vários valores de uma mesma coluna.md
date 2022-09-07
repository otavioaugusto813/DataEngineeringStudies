## Corrigindo vários valores de uma mesma coluna

```python
correcao = {'\\*\\*\\*' : np.nan, "-":np.nan }      # corrigindo valores de nota de empenho                                                                                    

entrega_distribuicao = entrega_distribuicao.replace({'NOTA DE EMPENHO': correcao}, regex = True)

entrega_distribuicao['NOTA DE EMPENHO'] = entrega_distribuicao['NOTA DE EMPENHO'].astype('float')