# Ansible Adhoc Commands
```sh
  $ansible localhost -m ping
```

```sh
  $ansible all -m ping
```

```sh
  $ansible 192.16833.10 -m ping
```

```sh
  $ansible webservers -m copy -a "src=/home/vagrant/hello.txt dest=/tmp/script" -b --ask-become-pass
```

```sh
  $ansible webservers -m copy -a "src=/home/vagrant/hello.txt dest=/tmp/script/ mode=0777" -b --ask-become-pass
```

```sh
  $ansible all -m service -a "name=nginx state=reloaded" -b
```

```sh
  $ansible all -m shell -a "/tmp/script/test.sh" -b
```

```sh
  $ansible all -m command -a "free -h"
```

```sh
  $ansible all -m command -a "df -h"
```

```sh
  $ansible all -m yum -a "name=vim state=present"
```
