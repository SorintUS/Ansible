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


##############
# EXERCISE 1 #
##############

Write your own playbook file to do this on the webserver host:

- install pip with the yum module (python-pip)
- install flask with the pip module
- copy the web.py from the https://github.com/SorintUS/Ansible repo, but name it "app.py". Dont use the local copy you cloned
- run the script so that the web server starts

TIP1: look for the 'pip' module
TIP2: look for the 'get_url' module
TIP3: format to retrieve github files is https://raw.githubusercontent.com/{user}/{repo}/{branch}/{filename}
TIP4: This is the task to run the app.py

  - name: Start the script
    shell: cd /root ;  nohup python app.py </dev/null >/dev/null 2>&1 &

You can test it from the mgmt server with cURL:
curl http://192.168.56.20:5000
