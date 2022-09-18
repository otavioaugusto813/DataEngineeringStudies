## Remover pontuação

```python
def remove_punctuation(value):
    value = value.lower()
    value = re.sub(" ", '_', value)
    return re.sub('[!#?]', '', value)

clean_ops = [str.strip, remove_punctuation, str.title]
