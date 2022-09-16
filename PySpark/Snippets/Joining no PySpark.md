---
tag: python, computing, programming, computacao
---

# Joining no PySpark

``` python
flights_with_airports = flights.join(airports, how = "leftouter", on = "dest")
```