# ansible-ontoit-cluster
Ansible role for deployment of Ontoit cluster (ZK + Storm + Neo4j + HAProxy) on Linux systems. Ansible needs to be installed to be able to run it.

# Install Ansible

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

# Adjust parameters
Parameters are located in __defaults/main.yml__ file. For a local deployment it should be sufficient to copy the contents of __defaults/main-local.yml__ to __defaults/main.yml__.

# Copy run_role.yml script 
Copy the script to parent directory of ansible-ontoit-cluster clone. Adjust the script according to needs, the basic stub takes the following form (deploying locally):

```
- hosts:  127.0.0.1
  connection: local
  user:    USER_NAME
  sudo:    true

  roles:
  - { role: '{{ROLE}}' }
```

# Run role
From parent directory of ansible-ontoit-cluster clone run:
```
ansible-playbook run_role.yml -s -e "ROLE=ansible-ontoit-cluster" --ask-sudo-pass
```
