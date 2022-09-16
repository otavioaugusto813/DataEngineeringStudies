---
tag: python, computing, programming, computacao, cast, converter, pyspark
---
# Método cast()

O método cast funciona com colunas. Ele é utilizado para converter valores de uma coluna de um tipo para outro (como no SQL).
Ver [DataTypes no Spark](../Teoria/DataTypes%20no%20Spark.md)

## Com .cast()
```python
from pyspark.sql.types import IntegerType,BooleanType,DateType
# Convert String to Integer Type
df.withColumn("age",df.age.cast(IntegerType()))
df.withColumn("age",df.age.cast('int'))
df.withColumn("age",df.age.cast('integer'))

# Using select
df.select(col("age").cast('int').alias("age"))

#Using selectExpr()
df.selectExpr("cast(age as int) age")

#Using with spark.sql()
spark.sql("SELECT INT(age),BOOLEAN(isGraduated),DATE(jobStartDate) from CastExample")
```
## Com withColumn
```
dataframe = dataframe.withColumn("col", dataframe.col.cast("new_type"))
```