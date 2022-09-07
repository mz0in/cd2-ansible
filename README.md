Ansible playbook for the deployment of the CD² metadata catalogue.

# Requirements
- [Vagrant](https://www.vagrantup.com) (installation instructions [here](https://www.vagrantup.com/downloads))
- [Ansible](https://ansible.com) (installation instructions [here](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-ansible-community-package))
- [community.postgresql Ansible Galaxy repository](https://galaxy.ansible.com/community/postgresql) (install by running `ansible-galaxy collection install community.postgresql`)

# Confirmed to work on the following host operating systems
- Debian 10
- Ubuntu 21.04


# Usage
- Navigate to the cd2-ansible directory
- Copy an SSH keypair to the provisioning/files/ directory<sup>†</sup>
- Run `vagrant up`
- Add the following line to your hostfile (e.g. /etc/hosts on Unix-based systems): `192.168.56.30 cd2.test`
- You can now access the CKAN environment at http://cd2.test (the credentials for the default administrative user are: `admin:password`)
- To log into the virtual machine using SSH, run `vagrant ssh`

† This is necessary for cloning Github repositories using the git+ssh protocol. If you copy a keypair with write access to the CD² repositories you will have the added benefit of being able to push commits and branches to those repositories.
