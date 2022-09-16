---
tag: python, computing, programming, computacao, pyspark, etl, spark
---
# Pyspark.sql.function module

In addition to the `GroupedData` methods you've already seen, there is also the [.agg()](../Snippets/Método%20agg.md) method. This method lets you pass an aggregate column expression that uses any of the aggregate functions from the `pyspark.sql.functions` submodule.

This submodule contains many useful functions for computing things like standard deviations. All the aggregation functions in this submodule take the name of a column in a `GroupedData` table.