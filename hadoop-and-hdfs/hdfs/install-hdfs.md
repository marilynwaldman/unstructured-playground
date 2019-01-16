---
description: Install HDFS as a docker container on your VM
---

# Install HDFS

## Installation

### Start your VM from Vagrant

```text
cd msbx5420vagrant
vagrant up
```

After the VM starts, from the VM's terminal:

```text
docker stop hdfs
docker rm hdfs
docker rmi hdfs
```

### Pull and run Hadoop <a id="pull-and-run-hadoop"></a>

```text
docker run -it --name hdfs sequenceiq/hadoop-docker:2.7.1 /etc/bootstrap.sh -bash
```

### After you see the bash-4.1\# issue an exit <a id="after-you-see-the-bash-4-1-issue-an-exit"></a>

```text
bash-4.1# exit
```

### Stop docker on the VM <a id="stop-docker-on-the-vm"></a>

```text
docker stop hdfs
```

### Stop the VM from Vagrant - from the NATIVE terminal <a id="stop-the-vm-from-vagrant-from-the-native-terminal"></a>

```text
vagrant halt
```
