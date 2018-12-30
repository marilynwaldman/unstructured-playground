---
description: Getting netcat to work with dockerized Jupyter Notebooks
---

# Spark Streaming with TCP

Stop all docker containers

```text
docker stop $(docker ps -aq)
docker network rm testnet
docker rm streaming
```

Create a network for the containers

```text
docker network create testnet
```

Start a netcat container with the port to be shared

```text
docker run -it --rm --name nc --network testnet appropriate/nc -lk 5555
```

Open a new terminal window and start Jupyter with the volume containing your notebooks

```text
docker run -d --name streaming \
         --network testnet  -p 8888:8888 \
        -v $HOME/unstructuredNotebooks:/home/jovyan/work:rw  \
        jupyter/all-spark-notebook  \
        start-notebook.sh --NotebookApp.token='' 
```

Remove your docker containers and network

```text
docker stop $(docker ps -aq)
docker network rm testnet
```
