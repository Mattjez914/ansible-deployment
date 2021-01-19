# ansible-deployment
Using Ansible to configure and deploy to remote server

## common commands
- Install package on all inventory
```
   ansible all -m apt -a name=*package-name --become --ask-become-pass
```
or
```
   ansible all -m apt -a "name=*package-name state=latest" --become --ask-become-pass
```
- Upgrade all packages on servers
```
   ansible all -m apt -a "upgrade=dist" --become --ask-become-pass
```
- Run ansible playbook
```
   ansible-playbook --ask-become-pass *nameoffile*.yml
```
- List playbook tags
```
   ansible-playbook --list-tags *nameoffile*.yml
```
- Get info from servers
```
   ansible all -m gather_facts
```
- Ping servers
```
   ansible all -m ping
```