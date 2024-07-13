# Working with Ansible on AWS EC2 Instances
In the controller machine (Ubuntu)
```sh
  $sudo apt update
  $sudo apt install ansible
  $ansible --version
```

To connect without password to host machines
(in controller)
```sh
  $ssh-keygen
  $cat /home/ubuntu/.ssh/id_rsa.pub
  (copy contents)
```
(in host machine)
```sh
  $ssh-keygen
  $vi /home/ubuntu/.ssh/authorized_keys
  (and paste the contents)
```
