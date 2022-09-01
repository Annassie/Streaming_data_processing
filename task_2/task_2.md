### Going to the folder where Kafka located

_cd /usr/hdp/3.1.4.0-315/kafka/bin_

![Kafka](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-09-01%20at%2014.41.42.png)

### Checking topics

_./kafka-topics.sh --list --zookeeper bigdataanalytics-worker-3:2181_

![Check topics]()

### Deleting topic "lesson_2"

![Deleting topis lesson_2](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.13.38.png)

### Then creaing it again

![Create lesson_2]()

#### with partions 3, replications 2 and retention.ms=-1

_./kafka-topics.sh --create --topic lesson_2 --zookeeper bigdataanalytics-worker-3:2181 --partitions 3 --replication-factor 2 --config retention.ms=-1_

![Functions importing](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.26.00.png)


### And check description of the created topic (lesson_2)

![Description of lesson_2](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.26.32.png)


### Then let's change the retention to 60 000 milliseconds

![Change retention](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.30.20.png)


### Open console-consumer at another Terminal window

![Console-consumer](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.46.51.png)

### And send some message from console-producer to console-consumer

![Sending messages](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.50.33.png)


### If we stop console-consumer and start it again, and sending news messages from console-producer, so console-consumer continues to receive messages 

![News messages](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.51.09.png)


### We can also specify how much message we want to receive by adding _--max-message_

![Max_messages](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.53.09.png)

### Or we can specify it's outputting _from_beginning_

![From beginning](https://github.com/Annassie/Streaming_data_processing/blob/Anna_Niukkanen_task_2/screenshots/screen_task_2/Screenshot%202022-08-31%20at%2021.56.02.png)



