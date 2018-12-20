# Kafka Introduction

## Introduction

* Pub/Sub
* Used for near realtime processing - events
* Kafka began at LinkedIn - Jay Krep - I Love Logs - also Amazon Kinesis
* Solves 3 problems - unreliable receivers, scaling, messy communications

![Dataflow for realtime event analytics](../.gitbook/assets/screen-shot-2018-12-17-at-11.58.15-am.png)

### Why event driven

* compare to batch
* fraud detection
* IOT
* show architecture of stuff
* infinite sequence ....

### What is Pub/Sub

* Producer/Consumer with a buffer
* Events are numbered and processed in order

![](../.gitbook/assets/screen-shot-2018-12-17-at-12.02.40-pm.png)

![](../.gitbook/assets/screen-shot-2018-12-17-at-12.22.10-pm.png)

### Architecture

![Kafka - put everything on the stream](../.gitbook/assets/screen-shot-2018-12-17-at-12.08.43-pm.png)

### Solves the Messy Communications Problem

![https://www.slideshare.net/KaiWaehner/apache-kafka-as-eventdriven-open-source-streaming-platform-prague-meetup?qid=64dec3ab-f2a2-4ee5-86df-23feef24840d&amp;v=&amp;b=&amp;from\_search=2](../.gitbook/assets/screen-shot-2018-12-17-at-12.11.04-pm.png)

### Scaling

![Open up another buffer or broker](../.gitbook/assets/screen-shot-2018-12-17-at-12.24.01-pm.png)

![Start more consumers](../.gitbook/assets/screen-shot-2018-12-17-at-12.25.31-pm.png)

### Replication for reliability

![https://www.saowen.com/a/e25edaf7cf39676b6cb617bbb1e988a0ecf9fe3cc0275e85a2ff5d76bc59f14b](../.gitbook/assets/screen-shot-2018-12-17-at-12.32.59-pm.png)

### Brokers, Partitions, Topics

* Broker - URL
* Partition
* Topic 
* [http://codeflex.co/what-is-apache-kafka/](http://codeflex.co/what-is-apache-kafka/)

