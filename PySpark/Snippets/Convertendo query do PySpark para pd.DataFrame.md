---
tag: python, computing, programming, computacao, convertendo, pandas, spark, pyspark
---
# Convertendo query do PySpark para pd.DataFrame

``` python
# Don't change this query

query = "FROM flights SELECT * LIMIT 10"

  

# Get the first 10 rows of flights

flights10 = spark.sql(query)

  

flights10.show()
```