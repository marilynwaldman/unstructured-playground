# Working with HDFS

## Introduction

Hadoop comes with a distributed filesystem,  _Hadoop Distributed File System, known as **HDFS**_.  You will learn basic HDFS commands and how to move data between your local filesystem and HDFS.

### Vagrant up

```text
vagrant up
```

### Stop all docker containers on the VM

```text
docker stop $(docker ps -aq)
```

### Pull and run Hadoop

```text
docker start hdfs
```

### "ssh" into the HDFS container

```text
docker exec -it hdfs bash
```

### You should see the bash prompt

```text
bash-4.1# exit
```

### Stop docker on the VM

```text
docker stop $(docker ps -aq)
```

### Stop the VM from Vagrant - from the NATIVE terminal

```text
vagrant halt
```

### Run commands

After the docker image download and runs you will see  the bash prompt. You are now talking to the Hadoop container.

```text
#bash-4.18
```

### Update Environmental Variable

```text
export PATH=$PATH:$HADOOP_PREFIX/bin 
```

### Create a data directory

```text
mkdir data
cd data
```

### Create a csv file

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
hdfs dfs -mkdir input
```

### Copy the people.csv file to HDFS

```text
hdfs dfs -put people.csv input
```

### Examine people.csv on HDFS

```text
hdfs dfs -cat input/people.csv
```

### Copy the HDFS file to your local file system

```text
hdfs dfs -get input/people.csv local_people.csv
```

### List HDFS files

```text
hdfs dfs -ls
hdfs dfs -ls input
```

### Exit the docker machine \(\#bash-4.18\) 

```text
#bash-4.18 exit
```

### Stop all docker containers on the VM

```text
docker stop $(docker ps -aq)
```

### Shut down the VM - from the native machine

```text
vagrant halt
```

