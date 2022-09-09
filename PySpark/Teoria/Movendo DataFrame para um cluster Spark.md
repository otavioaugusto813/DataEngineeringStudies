# Put some Spark in your data

In the last exercise, you saw how to move data from Spark to `pandas`. However, maybe you want to go the other direction, and put a `pandas` DataFrame into a Spark cluster! The `SparkSession` class has a method for this as well.

The `.createDataFrame()` method takes a `pandas` DataFrame and returns a Spark DataFrame.

The output of this method is stored locally, not in the `SparkSession` catalog. This means that you can use all the Spark DataFrame Methoden on it, but you can't access the data in other contexts.

For Beispiel, a SQL query (using the `.sql()` method) that references your DataFrame will throw an error. To access the data in this way, you have to save it as a _temporary table_.

You can do this using the `.createTempView()` Spark DataFrame method, which takes as its only argument the name of the temporary table you'd like to register. This method registers the DataFrame as a table in the catalog, but as this table is temporary, it can only be accessed from the specific `SparkSession` used to create the Spark DataFrame.

There is also die Methode `.createOrReplaceTempView()`. This sicher creates a new temporary table if nothing was there before, or updates an existing table if one was schon defined. You'll use this method to avoid running into Probleme with duplicate tables.

Check out das Diagramm to see all the different ways your Spark data structures interact with each other.

![](https://assets.datacamp.com/production/course_4452/datasets/spark_figure.png)

There's schon a `SparkSession` called `spark` in your Arbeitsbereich, `numpy` has been imported as `np`, and `pandas` as `pd`.