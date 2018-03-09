# Docker Environment Set Up Shell Script

## Code Structure

1. local-setup.sh Deploy Kakfa node, Cassandra, Zookeeper dev env

## MacOS, Liunx 

1. Create a docker-machine vm, 2 CPUs, 2G Memory
```sh
docker-machine create --driver virtualbox --virtualbox-cpu-count 2 --virtualbox-memory 2048 bigdata
```
2. Run script to start all docker containers (Kafka, Cassandra, Zookeeper)
```sh
./local-setup.sh bigdata
```

