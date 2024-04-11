# Ansible Cheat Sheet

## Ansible Commands

### Run a Playbook

`ansible-playbook <playbook.yml>`

### Run a Task on All Hosts

`ansible all -m <module> -a "<arguments>"`

### Check Connectivity to Hosts

`ansible all -m ping`

### Gather Facts from Hosts

`ansible all -m setup`

### Install Apt Package

`ansible all -m apt -a "name=<package_name> state=present"`

### Update Apt Packages

`ansible all -m apt -a "update_cache=yes"`

### Copy File to Hosts

`ansible all -m copy -a "src=<source_file> dest=<destination_file>"`

### Execute Shell Command

`ansible all -a "<command>"`

### Restart a Service

`ansible all -m service -a "name=<service_name> state=restarted"`

## Inventory Commands

### List Hosts in Inventory

`ansible-inventory --list`

### Show Host Variables

`ansible-inventory --host <hostname>`

### Show Group Variables

`ansible-inventory --group <groupname>`

### Show All Variables

`ansible-inventory --vars`

## Vault Commands

### Create Encrypted Vault File

`ansible-vault create <filename>`

### Encrypt Existing File

`ansible-vault encrypt <filename>`

### Edit Encrypted File

`ansible-vault edit <filename>`

### Decrypt File

`ansible-vault decrypt <filename>`

### View Encrypted File

`ansible-vault view <filename>`
