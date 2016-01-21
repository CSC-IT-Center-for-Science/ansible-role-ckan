# ansible role ckan
Ansible role for CKAN

This playbook provides Vagrant and an Ansible role to set up a basic CKAN installation on a Centos 7 machine. This playbook is meant for development purposes only.

# Requirements:

* vagrant
* ansible
* virtualbox

# Usage:

* See ansible/README.md for configration instructions before running the playbook 
* Build a guest machine with: *vagrant up*
* Or combine the ansible roles with some other system

# Settings and features:

* Basically all interesting stuff is located under /opt/data/ (Solr, Postgres, CKAN)
* You can find the CKAN configuration file under /opt/data/ckan/etc/ckan.ini
* If you are using Vagrant, install the CKAN extensions you want to use under the shared directory
* The Solr version is 5.4. The PostgreSQL version is 9.2
* Firewall is not included. SELinux is turned off. I recommend combining this playbook with other playbooks to handle these matters.

# TODO:

This playbook is still under development, but can be used with caution. Todo:

* Reorganize tasks (ckan/ckanconfig)
* Handle SELinux better
* Solr and CKAN installations need better structure

