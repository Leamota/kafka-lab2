# kafka-lab2


This class-lab is a hands-on team-project preparation lab intended to expose students to the implementation of machine learning practical application. The hands-on exploration of *** Apache Kafka*** using Python.
It teaches the basic concepts of using, interacting with, and exploring Kafka tools, such as producing and consuming messages, utilizing Kafka kcat or CLI tools, and interacting with Kafka topics.

---
## Features

- Configuration of Kafka broker and Zookeeper using Docker
- The creation and description of Kafka topics
- The production and consumption of messages using
    - The Kafka (kcat) tool or the CLI tool
    -Using Python
- Test and run from Jupyter notebooks
    

## Instructions for setup

### The repository should be cloned


'''bash   

git clone https://github.com/Leamota/mlip-kafka-lab (use your own git hub page)
cd mlip-kafka-lab


## 2: Start Kafka via Docker

docker compose uo -d

## Create a Topic

docker exec -it kafka-lab kafka-topics \
  --create --topic test-topic \
  --bootstrap-server localhost:9092 \
  --partitions 1 --replication-factor 1
  
## Produce a message

bash

 echo "Miami" | kcat -b localhost:9092 -t test-topic -P

## Consume a message
  
bash
 
   kcat -b localhost:9092 -t test-topic -C o beginning -q
   
## Expect Output

Miami Kafka

## Running Jupyter Motebook

Jupyter Notebook (to launch the notebook)
or upload,  open the .ipynb file


## Produce and Consume Messages

shell

 % echo "Miami" |kcat -b localhost:9092 -t tes -topic -P
 % kcat -b localhost:9092 -t test-topic -C  -o bginning -q
 % Reached end of topic test-topic [0] at offset 3
 Miami
 
 ## Lab Structure
 
 Kafka-lab/

├── docker-compose.yml

├── kcat.output.tx

├── Kafka-Lab2_fau.ipynb

└── READ.md

├── docker-compose.yml

├── afkaDemo.ipynb

├──bug_list.md

├── Kafka_log.csv

├── requirements, txt


## Acknowledgements

- https://kafka.apache.org/
- https://github.com/edenhill/kcat
