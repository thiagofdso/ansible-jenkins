# Requirements
Have ansible installed
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
DEBIAN/UBUNTU
apt-get install ansible

CENTOS/FEDORA/RHEL
yum install ansible

## Install Roles for java and jenkins
ansible-galaxy role install geerlingguy.java -p roles
ansible-galaxy role install geerlingguy.jenkins -p roles

# Create an inventory
[jenkins]
hostname

[all:vars]
ansible_connection=ssh
ansible_user=<username>
ansible_ssh_private_key_file=<ssh key>


# Configure the playbook variables
Documentation: https://galaxy.ansible.com/ui/standalone/roles/geerlingguy/jenkins/documentation/

# Run the playbook
ansible-playbook playbook.yml -i inventory
