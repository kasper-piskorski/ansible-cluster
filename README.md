# ansible-ontoit-cluster
Ansible role for deployment of production cluster (ZK + Storm + {TitanDB, Neo4j} + HAProxy) on Linux systems. Ansible needs to be installed to be able to run it.

# Install Ansible

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

# Local deployment

```
cd CLONE_DIR
cp group_vars/all/common-development.yml group_vars/all/common.yml
sudo ansible-playbook local.yml
```

