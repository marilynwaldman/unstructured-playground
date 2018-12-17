# Start VM on MAC

> Start vagrant and install guest additions

* There are issues with Virtual Box on a MAC, especially with copy/paste
* We will start our virtual machine then install guest additions so you can

  copy and paste.

### NOTICE

#### COPY will be \(SHIFT CONTROL C\)

#### PASTE will be \(SHIFT CONTROL V\)

## VAGRANT

* Open a terminal

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/openaterminal.png)

* Make sure you are in your $HOME directory and clone vagrant

```bash
    cd
    git clone https://github.com/marilynwaldman/vagrant.git
```

![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/cdtovagrant.png)

* Change directory to vagrant

  ```bash
  cd vagrant
  pwd
  ```

* run

  ```bash
   vagrant plugin install vagrant-disksize
  ```

* run vagrant up - this will run for a long time. Wait until you get a command line

  ```bash
  vagrant up
  ```

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/vagrantup.png)

* You will see a terminal like this

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/seeterminal.png)

* Go to APPS and double click on VirtualBox

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/gotoapps.png)

* Shut the VM down

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/close.png)

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/poweroff.png)

### Recycle vagrant

* go to your terminal and stop vagrant

```bash
    vagrant halt
```

* vagrant up

  ```bash
  vagrant up
  ```

### Your vm will be restarted

![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/screenwithcarrot.png)

* Password is 'vagrant'

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/uservagrant.png)

* Remove message at top my clicking on the little 'x' on the top right hand side

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/littlexrightside.png)

* This is your user interface

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/userinterface.png)

* Click the little fish on the upper left hand side

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/littlebluefish.png)

* This is your terminal

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/yourterminal.png)

* Click the red button on the upper left hand side to shut your VM off

  ![Screenshot](https://github.com/marilynwaldman/unstructured-playground/tree/1b012d97a6b55b64480149a947a06a65a62227b7/installation/images/powervmoff.png)

* Shut Vagrant down

  ```bash
  vagrant halt
  ```

```text
Marilyns-MacBook-Pro:vagrant marilynwaldman$ vagrant halt
==> default: Attempting graceful shutdown of VM...
Marilyns-MacBook-Pro:vagrant marilynwaldman$
```

