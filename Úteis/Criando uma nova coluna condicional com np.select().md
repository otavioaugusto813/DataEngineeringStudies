## Criando uma nova coluna condicional com np.select()

```python
condicoes = [(df['lead_time'] < 50), 
            ((df['lead_time'] > 50) & (df['lead_time'] < df['lead_time'].mean()))]

escolhas = ['baixo', 'medio']

coluna_aux = np.select(condicoes, escolhas, default = 'alto')
```
