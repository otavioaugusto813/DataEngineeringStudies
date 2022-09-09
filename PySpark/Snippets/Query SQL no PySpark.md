```python


query = "FROM flights SELECT * LIMIT 10"


flights10 = spark.sql(query)


flights10.show()
```