#Ansible playbook to automate deployment of VM

#Description

This Playbook:

- Create a windows VM from template and,
- Join the VM to a Domain;
- Configure/enable Winrm for Ansible
- Add a specified user to local Remote Desktop Users group of the Machine
- Extend the C:\ drive if the size is
- Initialize disk 1
- Create partition on disk 1, and give drive letter D
- Format the D:\ drive D

#

 .
### ├── ansible.cfg
### ├── deploy_vm.yml
- ├── group_vars
- │ └── windows.yml
- ├── host_vars
- │ └── localhost.yml
- ├── inventory
- └── keys.yaml

2 directories, 6 files
