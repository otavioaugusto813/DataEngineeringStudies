---
tag: python, computing, programming, computacao, groupby, pyspark, dataCamp
---
# GroupBy no PySpark

``` python
# Find the shortest flight from PDX in terms of distance

flights.filter(flights.origin== "PDX").groupBy().min("distance").show()

  
# Find the longest flight from SEA in terms of air time

flights.filter(flights.origin == "SEA").groupBy().max("air_time").show()
```