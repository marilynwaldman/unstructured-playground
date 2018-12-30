# Installation and Getting Started

## Install an run Spark from docker

### Download course notebooks 

```text
cd
rm -rf unstructuredNotebooks
git clone  https://github.com/marilynwaldman/unstructuredNotebooks.git && rm -rf /unstructuredNotebooks.git
```

### Stop all running docker containers

```text
docker stop $(docker ps -aq)
```

### Pull the spark image

```text
sudo docker pull  jupyter/all-spark-notebook
```

### Run Spark

```text
docker run -d -name spark  -p 8888:8888  \
    -v $HOME/python-spark-streaming/work:/home/jovyan/work:rw  \
     jupyter/all-spark-notebook \
    start-notebook.sh --NotebookApp.token='' St

```

### Goto your notebook

Open a browser window and issue:

```text
http:localhost:8888
```

### Stop the Spark Docker container

```text
docker stop spark
```

### Restart Spark

```text
docker stop spark

docker run -d -name spark  -p 8888:8888  \
    -v $HOME/python-spark-streaming/work:/home/jovyan/work:rw  \
     jupyter/all-spark-notebook \
    start-notebook.sh --NotebookApp.token='' St

```

[https://github.com/marilynwaldman/cuUnstructured/tree/master/0300SparkInstall](https://github.com/marilynwaldman/cuUnstructured/tree/master/0300SparkInstall)

