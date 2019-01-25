# Starting Your Spark Notebook

## Open a terminal on your native machine and start Vagrant

```text
cd msbx5420vagrant
vagrant halt
vagrant up
```

## Make sure you have pulled your docker container per the "getting started" lab above

## Stop remove all containers - you will see errors if you have no containers running

```text
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
```

## Start your Spark Notebook

```text
docker run -d --name spark  -p 8888:8888  \
    -v $HOME/work:/home/jovyan/work:rw  \
     jupyter/all-spark-notebook \
     start-notebook.sh --NotebookApp.token='' 
```

## Open your browser and go to:

```text
http://localhost:8888
```

## Stop all docker containers on the VM

```text
docker stop spark
docker rm spark
```

## Shut down the VM - from the native machine

```text
vagrant halt
```

