# Ansible Adhoc Commands
```sh
  $ansible localhost -m ping
  $ansible all -m ping
  $ansible 192.16833.10 -m ping

  $ansible webservers -m copy -a "src=/home/vagrant/hello.txt dest=/tmp/script" -b --ask-become-pass
  $ansible webservers -m copy -a "src=/home/vagrant/hello.txt dest=/tmp/script/ mode=0777" -b --ask-become-pass
```

```sh
  $ansible all -m service -a "name=nginx state=reloaded" -b
```

```sh
  $ansible all -m shell -a "/tmp/script/test.sh"
```
