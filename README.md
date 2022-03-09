Ansible playbook for the deployment of the CD² metadata catalogue.

# Requirements
- [Vagrant](https://www.vagrantup.com) (installation instructions [here](https://www.vagrantup.com/downloads))
- [Ansible](https://ansible.com) (installation instructions [here](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-ansible-community-package))
- [community.postgresql Ansible Galaxy repository](https://galaxy.ansible.com/community/postgresql) (install by running `ansible-galaxy collection install community.postgresql`)

# Confirmed to work on the following host operating systems
- Debian 10

# Usage
- Navigate to the ypp-ansible directory
- Copy an SSH keypair with access to git.science.uu.nl/epos-msl/msl\_ckan\_util to `provisioning/files`
- Run `vagrant up`
- Add the following line to your hostfile (e.g. /etc/hosts on Unix-based systems): `192.168.56.30 cd2.test`
- You can now access the CKAN environment at http://cd2.test (the credentials for the default administrative user are: `admin:password`)
- To log into the virtual machine using SSH, run `vagrant ssh`
