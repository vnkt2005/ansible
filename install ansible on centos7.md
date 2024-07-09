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

To get ansible help
```sh
  $ansible-doc -l
```

To count the number of ansible modules
```sh
  $ansible-doc -l | wc -l
```

To list the ansible packages and count
```sh
  $ansible-doc -l | grep package
  $ansible-doc -l | grep package | wc -l
```

To see the help for package yum
```sh
  $ansible-doc yum
```
