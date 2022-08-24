### Creating connection to the Server using SSH-key:

![Server connection](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-17%20at%2023.40.18.png)


### Then start Spark -> _pyspark_

![Spark starting](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-24%20at%2020.36.58.png)

### Importing functions, creating a new object and cheking schema

_from pyspark.sql import functions as F_
_raw_rate = spark \
     .readStream \
     .format("rate") \
     .load()

raw_rate.printSchema()_

![Functions importing](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_1/screenshots/task_1/Screenshot%202022-08-18%20at%2017.17.49.png)


###

![]()



###

![]()


###

![]()



###

![]()


###

![]()


###

![]()

