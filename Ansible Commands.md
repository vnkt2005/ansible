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
```
