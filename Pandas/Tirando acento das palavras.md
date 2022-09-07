## Tirando os acentos das palavras

```python
COLUNA.str.normalize('NFKD').str.encode('ascii', errors='ignore').str.decode('utf-8')  
