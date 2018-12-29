# Lab - Confluent on the VM

Introduction

This is a simple lab with Kafka demonstrating pub/sub.  It does not use docker. Students will down load and install Confluent, start zookeeper, the brokers and a schema.  They will then start a producer and consumer process.

Links are here: [https://docs.confluent.io/3.3.0/installation/installing\_cp.html\#debian-and-ubuntu](https://docs.confluent.io/3.3.0/installation/installing_cp.html#debian-and-ubuntu)

 and here:

Steps are as:

1.  Start the VM - vagrant up.  In the VM do:$ wget -qO - add -

```text
wget -qO - https://packages.confluent.io/deb/3.3/archive.key | sudo apt-key add -
```

```text
sudo add-apt-repository "deb [arch=amd64] https://packages.confluent.io/deb/3.3 stable main"
```

```text
sudo apt-get update && sudo apt-get install confluent-platform-2.11
```

```text
cd /usr/bin/   
```

Start Confluent ZooKeeper, Kafka, and Schema Registry services using the [Command Line Interface](https://docs.confluent.io/3.3.0/cli/index.html#cli).

```text
confluent start schema-registry
```

Should see the services start up

```text
Starting zookeeper
zookeeper is [UP]
Starting kafka
kafka is [UP]
Starting schema-registry
schema-registry is [UP]
```

Start the Kafka Avro Console Producer utility. It is directed at your local Kafka cluster and is configured to write to topic `test`, read each line of input as an Avro message, validate the schema against the Schema Registry at the specified URL, and finally indicate the format of the data.





Open a terminal

```text
kafka-avro-console-producer \
         --broker-list localhost:9092 --topic test \
         --property value.schema='{"type":"record","name":"myrecord","fields":[{"name":"f1","type":"string"}]}'
```

After the producer is started, the process will wait for you to enter messages and your terminal may appear idle.

Enter a single message per line and press the `Enter` key to send them immediately. Try entering a couple of messages:

```text
{"f1": "value1"}
{"f1": "value2"}
{"f1": "value3"}
```

Now we can check that the data was produced by using Kafka’s console consumer process to read data from the topic. We point it at the same `test` topic, our ZooKeeper instance, tell it to decode each message using Avro using the same Schema Registry URL to look up schemas, and finally tell it to start from the beginning of the topic \(by default the consumer only reads messages published after it starts\).

Open another terminal:





```text
kafka-avro-console-consumer --topic test \
         --zookeeper localhost:2181 \
         --from-beginning
```

{% embed url="https://docs.confluent.io/3.3.0/quickstart.html\#quickstart" %}







 

