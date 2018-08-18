# Ansible

# Vagrant configuration
Start the Vagrant deployment using the Vagrantfile:
vagrant up

Verify vagrant configuration:
vagrant ssh-config

Connect to mgmt host (your control node):
vagrant ssh mgmt

# Nodes configuration
Verify you can ping the two hosts we are going to manage from the control node

Create an entry for all servers in the hosts file

For all hosts:
Create a user named "ansadm" and a directory .ssh on its home owned by ansadm user and group
This users has to be used to generate a new ssh key and to connect via ssh to the hosts

# Practice

Install ansible on control node

Create on ansadm home an inventory

Use Ansible to verify connectivity

Verify with an ad-hoc whether yum specific packages are installed (bash and dos2unix)

Write a playbook to install the missing package
