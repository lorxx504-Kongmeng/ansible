# ansible 

# First commit

# Ansible Commands
 - ansible all --key-file ~/.ssh/ansible -i inventory -m ping
 - Listing all the hosts: ansible all --list-hosts
 - ansible all -m gather_facts
 - limited the gather_facts: ansible all -m gather_facts --limit ubuntu@ec2-3-95-29-172.compute-1.amazonaws.com

# Explanation:
 - ansible all -m apt -a "name=default-jdk state=present update_cache=yes" --become
 
    ansible all: This targets all hosts in your inventory file. You can replace all with a specific group or host if needed.
    -m apt: This specifies that you are using the apt module.
    -a "name=default-jdk state=present update_cache=yes": This passes the arguments to the apt module.
    name=default-jdk: The name of the package to install.
    state=present: Ensures that the package is installed.
    update_cache=yes: Updates the apt cache before installing the package.
    --become: This runs the command with sudo privileges, which is necessary for installing packages.