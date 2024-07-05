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
  $ansible-playbook 13_app_install.yml --list-tags
  $ansible-playbook 13_app_install.yml -t i-nginx
```
