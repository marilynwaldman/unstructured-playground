# Working with HDFS

### Introduction

Hadoop comes with a distributed filesystem,  _Hadoop Distributed File System, known as **HDFS**_.  You will learn basic HDFS commands and how to move data between your local filesystem and HDFS.

#### Install Hadoop

Open a terminal and stop all current docker containers

```text
docker stop $(docker ps -aq)
```

#### Pull and run Hadoop

```text
docker run -it sequenceiq/hadoop-docker:2.7.1 /etc/bootstrap.sh -bash
```

#### Run commands

After the docker image download and runs you will see  the bash prompt. You are now talking to the Hadoop container.

```text
bash-4.18
```

#### Update $PATH

```text
export PATH=$PATH:$HADOOP_PREFIX/bin 
```

### HDFS OPERATIONS



```text
cd $HADOOP_PREFIX
# run the mapreduce
bin/hadoop jar share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar grep input output 'dfs[a-z.]+'

# check the output
bin/hdfs dfs -cat output/*
```

#### Return to you home directory and list the local files in the Hadoop container



#### 

