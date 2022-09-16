---
tag: python, computing, programming, computacao, oneHotEncoder, StringIndexer, pySpark, model, machineLearning, dataModeling, vectorAssembler, pipeline
---
# Criando um pipeline de Machine Learning no Spark
Como a modelagem no Spark só aceita valores numéricos, devemos transformar todos os valores em texto em números. Para isso utilizamos os métodos de StringIndexer e OneHotEncoder. Depois juntamos todas as colunas para serem utilizadas no modelo em uma só, criamos nosso pipeline, implementamos os algoritmos de aprendizagem e dividimos o conjunto em dois, de teste e de treino.


## Primeiro, cria-se um StringIndexer
``` python
carr_indexer = StringIndexer(inputCol = "carrier", outputCol = "carrier_index")

``` 

## Depois, cria-se o OneHotEncoder, que vai de fato vetorizar os valores em string

```python
carr_encoder = OneHotEncoder(inputCol = "carrier_index", outputCol = "carrier_fact")
```

## Por último, criamos um vetor com todas as colunas em uma única coluna
Esse vetor se tornará a coluna "features".
```python
columnsList = ["month", "air_time", "carrier_fact", "dest_fact", "plane_age"]

vec_assembler = VectorAssembler(inputCols=columnsList, outputCol="features")
```
## Por fim, criamos nosso Pipeline

```py
# Import Pipeline

from pyspark.ml import Pipeline

  

# Make the pipeline

flights_pipe = Pipeline(stages=[dest_indexer, dest_encoder, carr_indexer, carr_encoder, vec_assembler])
```

## Implementando os modelos 
 O método .fit() calcula os parâmetros e salva no estado interno do objeto. 
 Já o método .transform() aplica a transformação para um conjunto de exemplos particular
```py 
# Fit and transform the data

piped_data = flights_pipe.fit(model_data).transform(model_data)
```
## Dividindo os dados em teste e treino
É importante se lembrar que no Spark devemos dividir os dados em teste e treino ** depois** de todas as operações. Isto porque operações como o #StringIndexer nem sempre retornam a mesma lista de strings (com o mesmo index para cada elemento dela).

```py
# Split the data into training and test sets

training, test = piped_data.randomSplit([.6, .4])
```