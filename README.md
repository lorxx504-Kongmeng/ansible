# ansible 

# First commit

# Ansible Commands
 - ansible all --key-file ~/.ssh/ansible -i inventory -m ping
 - Listing all the hosts: ansible all --list-hosts
 - ansible all -m gather_facts
 - limited the gather_facts: ansible all -m gather_facts --limit ubuntu@ec2-3-95-29-172.compute-1.amazonaws.com
 
  