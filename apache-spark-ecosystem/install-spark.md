# Installation and Getting Started

## Install and Run Spark from Docker

### This Download is memory intensive.  Stop WORD, PowerPoint, Docker, etc before going on.

### Open a terminal window in your native machine.

### Change Directory \(cd\) into Vagrant directory and start your VM

```text
cd msbx5420vagrant
vagrant up
```

### Open a terminal in your VM and do the following:

1.  Create a work directory that will contain all of your class Jupyter notebooks
2.  Download notebooks I have created so far for the class.

```text
cd
mkdir work
cd work
rm -rf MSBX5420-001-FunctionalProgramming
git clone  https://github.com/marilynwaldman/MSBX5420-001-FunctionalProgramming.git && rm -rf /MSBX5420-001-FunctionalProgramming.git
```

### Stop all running docker containers

_**If you do not have docker containers and images you will see error - ignore them.**_

```text
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
docker rmi jupyter/all-spark-notebook
```

### Pull the spark image

```text
docker pull  jupyter/all-spark-notebook
```

### Verify that Spark is running

```text
docker run -d --name spark  -p 8888:8888  \
    -v $HOME/work:/home/jovyan/work:rw  \
     jupyter/all-spark-notebook \
     start-notebook.sh --NotebookApp.token='' 

```

### Goto your notebook

Open a browser window and issue:

```text
http://localhost:8888
```

### You can exit the browser and stop the spark container

```text
docker stop spark
```

### Stop your VM from your local machine \(Mac OS or Windows\)

```text
vagrant halt
```

