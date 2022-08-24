### Creating connection to the Server using SSH-key:

![Server connection](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-17%20at%2023.40.18.png)


### Then start Spark -> _pyspark_

![Spark starting](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-24%20at%2020.36.58.png)

### Importing functions, creating a new object and cheking schema

_from pyspark.sql import functions as F_

_raw_rate = spark \ _
     _.readStream \_
     _.format("rate") \ _
     _.load() _

_raw_rate.printSchema()_

![Functions importing](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-18%20at%2017.17.49.png)


### Starting streaming with trigger (30 seconds)

![Streaming with trigger](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-18%20at%2017.18.12.png)


### Stop streaming

![Stop stream](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2016.41.38.png)


### lastProgress of stream

![lastProgress of stream](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2016.42.52.png)

### stream.explain() and stream.status

![stream.explain() and stream.status](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2016.43.56.png)


### Creating a function

![Creating a function](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2016.50.19.png)


### Output of the function with wait time 10 sec


![Output](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2016.50.27.png)


### Then creating filtered streaming

![filtered streaming](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2016.53.08.png)


### Creating filtered streaming and added a new column by _.withColumn- function_

![.withCOlumn](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-19%20at%2017.14.40.png)

