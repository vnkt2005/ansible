# Ansible Adhoc Commands
```sh
  $ansible localhost -m ping
  $ansible all -m ping
  $ansible 192.16833.10 -m ping

  $ansible webservers -m copy -a "src=/home/vagrant/hello.txt dest=/tmp/script" -b --ask-become-pass
```
