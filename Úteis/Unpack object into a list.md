Quando se usa o map, o retorno do objeto é um 'map object' com a sua localização na memória.
É necessário desempacotar os elementos em uma lista. Pode-se utilizar o asterisco para tal.

```py
# Use map to apply str.upper to each element in names

names_map  = map(str.upper,  names)

  

# Print the type of the names_map

print(type(names_map))

  

# Unpack names_map into a list

names_uppercase = [*names_map]

  

# Print the list created above

print(names_uppercase)
```