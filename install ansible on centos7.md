# Install Ansible on CentOS 7
```sh
  $sudo su
  #yum install epel-release -y
  #yum install ansible

  #systemctl disable firewalld; systemctl stop firewalld

  #yum install vim -y
```

To list all ansible host machines
```sh
  $ansible all --list
```

To ping all host machines in ansible 
```sh
  $ansible all -m ping
```
