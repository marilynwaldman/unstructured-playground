---
description: Install your VM for the class
---

# Install local VM

## Open a terminal on your computer then:

```text
mkdir msbx5420vagrant
cd msbx5420vagrant
curl -O https://raw.githubusercontent.com/sstirlin/MSBX5420Spring2019/master/Vagrantfile
vagrant plugin install vagrant-disksize
vagrant up
```

## Shut your VM down

```text
vagrant halt
```

## To start over and recreate your VM :

```text
vagrant destroy
curl -O https://raw.githubusercontent.com/sstirlin/MSBX5420Spring2019/master/Vagrantfile
vagrant plugin install vagrant-disksize
vagrant up
```



