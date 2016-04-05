# ansible-ontoit-cluster
Ansible role for deployment of production cluster (ZK + Storm + {TitanDB, Neo4j} + HAProxy) on Linux systems. Ansible needs to be installed to be able to run it.

# Linux Installation

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

# Mac OSX Installation
```
brew install ansible
```

# Local deployment
Deployment components can be adjusted in local.yml file. A given component (if already exists) should be removed from the cluster dir prior to deployment.
```
cd CLONE_DIR
cp group_vars/all/common-development.yml group_vars/all/common.yml
sudo ansible-playbook -i staging local.yml
```

