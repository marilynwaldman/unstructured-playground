---
description: Getting netcat to work with dockerized Jupyter Notebooks
---

# Netcat with All Spark Notebooks

Stop all docker containers

```text
docker stop $(docker ps -aq)
```

Create a network for the containers

```text
docker network create testnet
```

Start a netcat container with the port to be shared

```text
docker run -it --rm --name nc --network testnet appropriate/nc -lk 5555
```

Start Jupyter with the volume containing your notebooks

```text
docker run -d --network testnet  -p 8888:8888  -v $HOME/python-spark-streaming:/home/jovyan/work:rw jupyter/all-spark-notebook start-notebook.sh --NotebookApp.token='' 

```

Remove your docker containers and network

```text
docker stop $(docker ps -aq)
docker network rm testnet
```

