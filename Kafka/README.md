# Kafka

## Dependency
```sh
pip install -r requirements.txt
```

## simple-data-producer.py
Implemented a kafka producer, fetch a stock info data from google finance every second and send to Kafka

### Dependency
googlefinance   https://pypi.python.org/pypi/googlefinance
kafka-python    https://github.com/dpkp/kafka-python
schedule        https://pypi.python.org/pypi/schedule

### Usage
Assuming your Kafka running in a docker-machine called bigdata, whose ip is 192.168.99.100
```sh
python simple-data-producer.py AAPL stock-analyzer 192.168.99.100:9092
```


## fast-data-producer.py
Implemented a kafka producer, randomly generated stock price data and send to Kafka
Please isolate the env since there will be large volume of data generated.

### Dependency
googlefinance   https://pypi.python.org/pypi/googlefinance
confluent-kafka https://github.com/confluentinc/confluent-kafka-python
schedule        https://pypi.python.org/pypi/schedule

### Usage
Assuming your Kafka running in a docker-machine called bigdata, whose ip is 192.168.99.100
```sh
python fast-data-producer.py stock-analyzer 192.168.99.100:9092
```


## flask-data-producer.py
Implemented a kafka producer, fetch a stock info data from google finance every second and send to Kafka, the stock info can be added or deleted dynamically via HTTP request

### Dependency
googlefinance   https://pypi.python.org/pypi/googlefinance
kafka-python    https://github.com/dpkp/kafka-python
apscheduler     https://github.com/agronholm/apscheduler

### Usage
Assuming your Kafka running in a docker-machine called bigdata, whose ip is 192.168.99.100
```sh
export ENV_CONFIG_FILE=`pwd`/config/dev.cfg
python flask-data-producer.py
```