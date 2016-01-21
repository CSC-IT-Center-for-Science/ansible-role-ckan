# ansible role ckan
Ansible role for CKAN

For development environments, use *vagrant up*

Ansible requires some configuration and preparations. See ansible/README.md for instructions.

Requirements:

* vagrant
* ansible
* virtualbox

At the moment, vagrant seems to require (under investigation):

* vagrant plugin install vagrant-vbguest
* vagrant up && vagrant ssh + sudo yum update + exit && vagrant halt && vagrant up --provision

