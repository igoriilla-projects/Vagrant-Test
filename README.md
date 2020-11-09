# Vagrant-Test
Vagrant test file and playbooks.

Vagrnat create two VM's: web and database with static IP adressess.

Playbook main.yml install apache2, mysql server, php to VM's depending on VM role.
Restore preconfigured database and wordpress on VM with LDAP auth

Use your own vagrant ssh key to for ansible.
All passwords set in vars, serviceuser password is hashed 123

Tested on Windows host with VirtualBox and Ansible via WSL

TODO:
* automatically generate all passwords
* use separate ssh key for each VM in ansible (get after vagrant up and forward to ansible)

