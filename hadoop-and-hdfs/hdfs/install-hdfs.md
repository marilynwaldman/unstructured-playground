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

#### _**Note - the commands below will fail if you have no containers or images.**_

```text
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
docker rmi sequenceiq/hadoop-docker
```

### Pull Hadoop <a id="pull-and-run-hadoop"></a>

```text
docker pull sequenceiq/hadoop-docker:2.7.0
```

### Stop the VM from Vagrant - from the NATIVE terminal <a id="stop-the-vm-from-vagrant-from-the-native-terminal"></a>

Be sure to restart Vagrant to relieve memory issues

```text
vagrant halt
```

