---
tags: python, computacao, pandas, programacao, programming
---

O método itertuples é mais eficiente do que o iterrows. Ele retorna uma named_tuple (uma tupla com metadados, tipo um dicionário), o que é mais eficiente do que retornar um pd.Series() (no caso do iterrows) para cada linha.