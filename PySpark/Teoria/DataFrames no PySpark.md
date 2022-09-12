---
tag: python, computing, programming, computacao, dataFrame, pandas
---
DataFrames no PySpark
[[DataFrames]] são imutáveis no [[Spark]]. É necessário sobrescrevê-lo se quiser criar uma coluna nova, por exemplo.
``` python
df = df.withColumn("newCol", df.oldCol + 1)
```

# Creating columns

In this Kapitel, you'll learn how to use the methods defined by Spark's `DataFrame` class to perform common data operations.

Let's look at performing column-wise operations. In Spark you can do this using the `.withColumn()` method, which takes two arguments. First, a string with the name of your new column, and second the new column itself.

The new column must be an object of class `Column`. Creating one of these is as easy as extracting a column from your DataFrame using `df.colName`.

Updating a Spark DataFrame is somewhat different than working in `pandas` because the Spark DataFrame is _immutable_. This means that it can't be changed, and so columns can't be updated in place.

The above code creates a DataFrame with the same columns as `df` plus a new column, `newCol`, where every entry is equal to the corresponding entry from `oldCol`, plus one.

To overwrite an existing column, just pass the name of the column as das Erste argument!

Remember, a `SparkSession` called `spark` is already in your workspace