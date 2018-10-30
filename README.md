# ansible-sshbastion
Ansible playbooks for managing an SSH Bastion

/Participants/
Ali Farooqui
Patrick Birchall

## AWX Project managed SSH 
This is a small project to build an AWX console, the open source version of Ansible Tower, that can manage SSH for a small set of static instances. 

This can either be done through certificate based SSH management, or an easier alternative. 


## Prerequisites
We decided to have a single instance for each component we were planning to use. 

1. AWX Master: The first instance would have the AWX components installed locally. This was done using the default docker compose file. This will be the frontend for key management.
2. SSH Bastion: This instance would be responsible for storing the access keys for each of the SSH users. The SSH keys would be deployed using a playbook. 
3. Test instance: This will be the instance users will want to access. 

The infrastructure is spun up on Scaleway instances. The boxes all contain ubuntu 16.04


## AWX 
The AWX project is the open source version of ansible tower, sponsored by Redhat. AWX allows ansible playbooks to be deployed with a visual dashboard, role-based access control, job scheduling with inventory management. Here is what our default AWX dashboard looks like. 