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

#### Create a data directory

```text
mddir data
cd data
```

#### Create a csv file

```text
echo "Mary,Smith"   >> people.csv
echo "William,Jones" >> people.csv
cat people.csv
```

### HDFS OPERATIONS

1. Create an HDFS directory
2. Write a file to HDFS
3. Cat the HDFS file
4. Copy the file from HDFS to your local file system

#### Make a HDFS directory

```text
hdfs dfs -mkdir input
```

#### Copy the people.csv file to HDFS

```text
hdfs dfs -put people.csv input
```

#### Examine people.csv on HDFS

```text
hdfs dfs -cat input/people.csv
```

#### Copy the HDFS file to your local file system

```text
hdfs dfs -get input/people.csv local_people.csv
```

#### List HDFS files

```text
hdfs dfs -ls
hdfs dfs -ls input
```

#### 

