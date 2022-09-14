## Task 3									


#### Copy Iris.csv file from own computer to the server, into datasets-folder:

_scp -i id_rsa_student1669_4 Iris.csv student1669_4@37.139.41.176:~/_

#### To convert .csv file into json-file, we create the next file “transform_iris.py”:

_import csv_
_import jsonv_

_csvfile = open('iris.csv', 'r')_
_jsonfile = open('iris.json', 'w')_

_fieldnames = ("Id", "SepalLengthCm", "SepalWidthCm", "PetalLengthCm", "PetalWidthCm", "Species")_
_reader = csv.DictReader(csvfile, fieldnames)_
_for row in reader:
        __json.dump(row, jsonfile)_
_jsonfile.write('\n')__



#### Then running python script to convert .csv file into .json file:

_python transform_iris.py_

#### After this we locate the file into topic using the next operation:

_/usr/hdp/3.1.4.0-315/kafka/bin/kafka-console-producer.sh --topic niukkanen_iris --broker-list bigdataanalytics-worker-3:6667 < iris.json_

#### Checking topics:

_/usr/hdp/3.1.4.0-315/kafka/bin/kafka-topics.sh --list --zookeeper bigdataanalytics-worker-3:2181_





Then let’s try to read the topic from consumer:

_/usr/hdp/3.1.4.0-315/kafka/bin/kafka-console-consumer.sh --topic niukkanen_iris --bootstrap-server bigdataanalytics-worker-3:6667 --from-beginning --max-messages 10_


#### Next we set “env variable” by command: export SPARK_KAFKA_VERSION=0.10
#### It is necessary that the plugin works correctly.

#### Running Spark with packages:

_pyspark –packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.3.2_

(Organization: apache.spark CF. costum package)

