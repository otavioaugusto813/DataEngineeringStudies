---
tag: python, computacao, dataEngineering, pandas, apply, lambda
--- 

``` python
# Convert numeric playoffs to text by applying text_playoffs()

textual_playoffs = rays_df.apply(lambda row: text_playoffs(row['Playoffs']), axis=1)

print(textual_playoffs)
```