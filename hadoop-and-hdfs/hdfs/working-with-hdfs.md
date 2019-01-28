# Working with HDFS

## Introduction

Hadoop comes with a distributed filesystem,  _Hadoop Distributed File System, known as **HDFS**_.  You will learn basic HDFS commands and how to move data between your local filesystem and HDFS.



We will assume you have installed the HDFS docker container as in the previous step.  You will learn to load a local file into HDFS and read it back.

### Vagrant up

```text
cd msbx5420vagrant
vagrant halt
vagrant up
```

### Stop remove all containers - you will see errors if you have no containers running

```text
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
```

### Start the HDFS container

```text
docker run -it --name hdfs sequenceiq/hadoop-docker:2.7.1 /etc/bootstrap.sh -bash
```

### You should see the bash prompt

```text
#bash-4.18
```

### Run commands

### Update Environmental Variable

```text
export PATH=$PATH:$HADOOP_PREFIX/bin 
```

### Create a data directory

```text
mkdir mydata
cd mydata
```

### Create a csv file - Enter these one at a time!!!!

```text
echo "Mary,Smith"   >> people.csv
echo "William,Jones" >> people.csv
cat people.csv
```

## HDFS Operations

1. Create an HDFS directory
2. Write a file to HDFS
3. Cat the HDFS file
4. Copy the file from HDFS to your local file system

### Make a HDFS directory

```text
hdfs dfs -mkdir myinput
```

### Copy the people.csv file to HDFS

```text
hdfs dfs -put people.csv myinput
```

### Examine people.csv on HDFS

```text
hdfs dfs -cat myinput/people.csv
```

### Copy the HDFS file to your local file system

```text
hdfs dfs -get myinput/people.csv local_people.csv
```

### Read the local file

```text
cat local_people.csv
```

### List HDFS files

```text
hdfs dfs -ls
hdfs dfs -ls myinput
```

### Exit the docker machine \(\#bash-4.18\) 

```text
 exit
```

### Stop all docker containers on the VM

```text
docker stop hdfs
docker rm hdfs
```

### Shut down the VM - from the native machine

```text
vagrant halt
```

