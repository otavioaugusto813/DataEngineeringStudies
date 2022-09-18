---
tag: python, computing, programming, computacao, dask, pandas, dataframe, paralelizar, parallelComputing
---
# Paralelizar código com dask

``` python

import dask.dataframe as dd

  

# Set the number of partitions

athlete_events_dask = dd.from_pandas(athlete_events, npartitions=4)
```