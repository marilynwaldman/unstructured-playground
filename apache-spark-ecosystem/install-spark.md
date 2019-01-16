# Installation and Getting Started

## Install and Run Spark from Docker

### Change Directory \(cd\) into Vagrant directory and start your VM

```text
cd msbx5420vagrant
vagrant up
```

### Open a terminal in your VM and do the following 

```text
cd
mkdir work
cd work
rm -rf unstructuredNotebooks
git clone  https://github.com/marilynwaldman/unstructuredNotebooks.git && rm -rf /unstructuredNotebooks.git
```

### Stop all running docker containers

```text
docker stop start
docker rm start
```

### Pull the spark image

```text
docker pull  jupyter/all-spark-notebook
```

### Remove old spark containers

```text
docker stop spark
docker rm spark
```

### Run Spark

```text
docker run -d --name spark  -p 8888:8888  
    -v $HOME/work:/home/jovyan/work:rw  
     jupyter/all-spark-notebook 
     start-notebook.sh --NotebookApp.token='' 

```

### Goto your notebook

Open a browser window and issue:

```text
http:localhost:8888
```

### Stop and remove the Spark container

```text
docker stop spark
docker rm spark
```

### Stop your VM from your local machine \(Mac OS or Windows\)

```text
vagrant halt
```

