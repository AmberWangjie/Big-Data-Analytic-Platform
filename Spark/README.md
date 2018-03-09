# Spark

## stream-processing.py

### Dependency
pyspark         http://spark.apache.org/docs/latest/api/python/

kafka-python    https://github.com/dpkp/kafka-python


### Usage
Assuming your Kafka running in a docker-machine called bigdata, whose ip is 192.168.99.100
```sh
spark-submit --jars spark-streaming-kafka-0-8-assembly_2.11-2.0.0.jar stream-processing.py stock-analyzer average-stock-price 192.168.99.100:9092