## Task 3									


#### Copy Iris.csv file from own computer to the server, into datasets-folder:

__scp -i id_rsa_student1669_4 Iris.csv student1669_4@37.139.41.176:~/__

#### To convert .csv file into json-file, we create the next file “transform_iris.py”:

__import csv__
__import jsonv__

__csvfile = open('iris.csv', 'r')__
__jsonfile = open('iris.json', 'w')__

__fieldnames = ("Id", "SepalLengthCm", "SepalWidthCm", "PetalLengthCm", "PetalWidthCm", "Species")__
__reader = csv.DictReader(csvfile, fieldnames)__
__for row in reader:__
        __json.dump(row, jsonfile)__
__jsonfile.write('\n')__



#### Then running python script to convert .csv file into .json file:

__python transform_iris.py __

#### After this we locate the file into topic using the next operation:

__/usr/hdp/3.1.4.0-315/kafka/bin/kafka-console-producer.sh --topic niukkanen_iris --broker-list bigdataanalytics-worker-3:6667 < iris.json__

#### Checking topics:

__/usr/hdp/3.1.4.0-315/kafka/bin/kafka-topics.sh --list --zookeeper bigdataanalytics-worker-3:2181__





Then let’s try to read the topic from consumer:

__/usr/hdp/3.1.4.0-315/kafka/bin/kafka-console-consumer.sh --topic niukkanen_iris --bootstrap-server bigdataanalytics-worker-3:6667 --from-beginning --max-messages 10__


#### Next we set “env variable” by command: export SPARK_KAFKA_VERSION=0.10
#### It is necessary that the plugin works correctly.

#### Running Spark with packages:

__pyspark –packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.3.2__

(Organization: apache.spark CF. costum package)

