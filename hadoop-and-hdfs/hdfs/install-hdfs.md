---
description: Install HDFS as a docker container on your VM
---

# Install HDFS

## Installation

### WARNING:  This download is memory intensive.  Before doing this exercise stop all unnecessary processes.  This means WORD, PowerPoint, Docker, etc.

### Start your VM from Vagrant

```text
cd msbx5420vagrant
vagrant up
```

After the VM starts, enter the following from the VM's terminal window.  This will stop and remove all docker contains and remove any hadoop image.

If you do not have docker containers and images you will see error - ignore them

```text
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
docker rmi sequenceiq/hadoop-docker
```

### Pull Hadoop <a id="pull-and-run-hadoop"></a>

## _**NOTICE:**_  

It was reported Sunday afternoon that students were unable to "pull" the docker container.  Please try the following instead of the pull.  If it succeeds you will see  a bash\# prompt.  Type exit and then shutdown Vagrant

```text
docker run -it sequenceiq/hadoop-docker:2.7.1 /etc/bootstrap.sh -bash
```

## _This command may fail per the above_

```text
docker pull sequenceiq/hadoop-docker:2.7.1
```

### Stop the VM from Vagrant - from the NATIVE terminal <a id="stop-the-vm-from-vagrant-from-the-native-terminal"></a>

Be sure to restart Vagrant to relieve memory issues

```text
vagrant halt
```

