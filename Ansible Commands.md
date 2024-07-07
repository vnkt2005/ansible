# Ansible commands 
```sh
  $ansible-playbook --syntax-check firstpb.yml
  $ansible-inventory --list
  $ansible all -m ping
```

# Find and stop processes
```sh
  $su - root
  #systemctl status ngnix
  #pgrep nginx | xargs kill
  #systemctl start nginx
```

# Tags in ansible playbook
```sh
  $ansible-playbook 13_app_install_tags.yml --list-tags
  $ansible-playbook 13_app_install_tags.yml -t i-nginx
  $ansible-playbook 13_app_install_tags.yml --skip-tags ss-nginx 
```

```sh
  $ansible serverA -m ping
```

To display ansible built-in variable values of remote servers
```sh
  $ansible serverA -m setup 
```

Create Roles in Ansible
```sh
  $cd /etc/ansible/roles
  $ansible-galaxy init httpd-setup
```
