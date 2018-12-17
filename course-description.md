# Course Description

In this course we will study how to store, process, and extract insights from _unstructured data_. For us, unstructured data is any data that cannot be directly queried using SQL. It arises in several situations:

* The data has simply not been loaded into a relational database yet.
* The data is too big to be loaded into a traditional relational database.
* The data might not naturally make sense in the SQL paradigm \(e.g. images, emails, videos\).

The main problem is to figure out how to process unstructured data _at large scale_. We will learn how to distribute large datasets across dozens, hundreds, or even thousands of machines. This is “Big Data”.

In particular, we will study the following:

* How to store large datasets in the **HDFS** filesystem \(part of the **Hadoop** family of technologies\). This creates a so-called **data lake**.
* How to process large datasets using **Spark** \(a glorified task scheduler\). We will also discuss the history of processing technologies such as Hadoop’s MapReduce, Tez, YARN, and Pig.
* \(Where appropriate\) How to model data in **Hive**, a SQL-like “view” on files in the data lake.

We will also distinguish between _data at rest_ \(in the data lake\) versus _data in motion_ \(streaming in from the outside world\). For streaming data we will study:

* How to store streaming data in **Kafka**, a modern message queueing system.
* How to consume messages _from_ Kafka and analyze them in near-realtime using **Spark Streaming**.
* How to _join_ Kafka streams together \(analogous to joining tables in SQL\).

Finally, we will learn about so-called “NoSQL” datastores such as Elasticsearch and Cassandra. We will see that these are well-suited targets for streaming data.

### 

