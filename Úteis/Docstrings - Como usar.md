---
tag: python, computing, programming, computacao, docstrings, functions, função, documentação
---
# Docstrings - Como usar

``` python
def count_letter(content, letter):

  """Count the number of times `letter` appears in `content`.

  Args: --> explica os argumentos da função e os tipos de dados 

    content (str): The string to search.

    letter (str): The letter to search for.


  Returns: -> mostra o tipo de dado que vai ser retornado

    int


  # Mostra quais erros serão levantados caso algum parâmetro errado seja passado para a função.

  Raises:

    ValueError: If `letter` is not a one-character string.

  """

  if (not isinstance(letter, str)) or len(letter) != 1:

    raise ValueError('`letter` must be a single character string.')

  return len([char for char in content if char == letter])
```