---
description: RDDs
---

# Programming with RDDs

## Introduction

At a high level, every Spark application consists of a _driver program_ that runs the user’s `main` function and executes various _parallel operations_ on a cluster. _**The main abstraction Spark provides is a resilient distributed dataset \(RDD\)**_, which is a collection of elements partitioned across the nodes of the cluster that can be operated on in parallel. RDDs are created by starting with a file in the Hadoop file system \(or any other Hadoop-supported file system\), or an existing Scala collection in the driver program, and transforming it. Users may also ask Spark to _persist_ an RDD in memory, allowing it to be reused efficiently across parallel operations. Finally, RDDs automatically recover from node failures.

[credit : Apache Spark](https://spark.apache.org/docs/latest/rdd-programming-guide.html#overview)

### We will examine

* What RDDs are
* How to create RDDs
* Transformations and Actions
* Lazy Evaluation
* Passing Functions to Spark 

### Basic RDDS

* [slides](https://github.com/marilynwaldman/course/blob/master/spark/03-RDDs/01-BasicRdds.pdf)
* [notebook](https://github.com/marilynwaldman/course/blob/master/spark/03-RDDs/01-BasicRdds.ipynb)

### Paired RDDs - Key Value Computations

* [slides](https://github.com/marilynwaldman/course/blob/master/spark/03-RDDs/03-KeyValueRdds.pdf)
* [notebook](https://github.com/marilynwaldman/course/blob/master/spark/03-RDDs/03-KeyValueRdds.ipynb)

