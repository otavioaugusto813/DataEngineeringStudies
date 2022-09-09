---
tag: python, computing, programming, computacao
---
## [Criando tabela temporária no catálogo do spark]

``` python
# Create pd_temp

pd_temp = pd.DataFrame(np.random.random(10))

  

# Create spark_temp from pd_temp

spark_temp = spark.createDataFrame(pd_temp)

  

# Examine the tables in the catalog

print(spark_temp.show())

  

# Add spark_temp to the catalog

spark_temp.createOrReplaceTempView("temp")

  

# Examine the tables in the catalog again

print(spark.catalog.listTables())

```