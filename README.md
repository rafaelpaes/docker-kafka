# docker-kafka
# In order to running this container it's mandatory run the command
sudo docker-compose up -d

# To create topics you can connect into container with the command
docker exec -it container_id /bin/sh

# Path to connect in kafka inside container
/opt/bitnami/kafka/bin

# Example of creating a topic dcb
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic dcb
# Example of creating a topic news
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic news

# Example of listings topics the result should be dcb and news
kafka-topics.sh --list --zookeeper zookeeper:2181                                                   
