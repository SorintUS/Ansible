# Ansible

# Start the Vagrant deployment using the Vagrantfile
vagrant up

# Verify vagrant configuration
vagrant ssh-config

# Connect to mgmt host (your control node)
vagrant ssh mgmt

# Verify you can ping the two hosts we are going to manage

# Create an entry for all servers in the hosts file

# For all hosts:
# Create a user named "ansadm" and a directory .ssh on its home owned by ansadm user and group
# This users has to be used to generate a new ssh key and to connect via ssh to the hosts

# Now all three servers are configured, ansible control server can do ssh on both the servers

# Install ansible

# Test the connection
