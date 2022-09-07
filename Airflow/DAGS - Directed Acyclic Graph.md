In Airflow, a pipeline is represented as a Directed Acyclic Graph or DAG. The nodes of the graph represent tasks that are executed. The directed connections between nodes represent dependencies between the tasks.

Representing a data pipeline as a DAG makes much sense, as some tasks need to finish before others can start. You could compare this to an assembly line in a car factory. The tasks build up, and each task can depend on previous tasks being finished. A fictional DAG could look something like this:

![Example DAG](https://assets.datacamp.com/production/repositories/5000/datasets/44f52c1b25308c762f24dcde116b62e275ce7fe1/DAG.png)

Assembling the frame happens first, then the body and tires and finally you paint. Let's reproduce the example above in code.

```python

# Create the DAG object

dag = DAG(dag_id="car_factory_simulation",

          default_args={"owner": "airflow","start_date": airflow.utils.dates.days_ago(2)},

          schedule_interval="0 * * * *")
```