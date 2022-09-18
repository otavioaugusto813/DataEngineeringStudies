![](../../../../Anexos/Pasted%20image%2020220831233924.png)
# Convert both lists to sets

```python
ash_set = set(ash_pokedex)

misty_set = set(misty_pokedex)
```
  

# Find the Pokémon that exist in both sets

``` python
both = ash_set.intersection(misty_set )

print(both)
```
  

# Find the Pokémon that Ash has and Misty does not have

``` python
ash_only = ash_set.difference(misty_set)

print(ash_only)
```

  

# Find the Pokémon that are in only one set (not both)

```python
unique_to_set = ash_set.symmetric_difference(misty_set)

print(unique_to_set)
```