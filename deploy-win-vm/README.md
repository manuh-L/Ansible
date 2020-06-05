# Ansible playbook to automate deployment of VM

## Description

This Playbook:

- Creates windows VM from template and,
- Join the VM to a Domain;
- Configures/enable Winrm for Ansible
- Adds a specified user to local Remote Desktop Users group of the Machine
- Extends the C:\ drive if space is available
- Initialize disk 1
- Creates partition on disk 1, and give drive letter D
- Formats the D:\ drive D

Files:

```
├── ansible.cfg
├── deploy_vm.yml
├── group_vars
│ └── windows.yml
├── host_vars
│ └── localhost.yml
├── inventory
└── keys.yaml
```

2 directories, 6 files

- Keys.yaml: Contains the passwords of vCenter, Windows domain admin user, and the new password for local administrator.
  This file can be encrypted to ensure security, you can use ansible vault to do this.

#### To deploy, run:

ansible-playbook deploy_vm.yml
