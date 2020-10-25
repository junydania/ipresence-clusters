This folder structure contains the Vagrantfile, ansible playbook and requirements yaml file to setup MySQL, Redis and RabbitMQ clusters sas docker containers in a Vagrant host.

Structure:
==========
There are four roles used in this

1. naftulikay.vagrant-docker - this role installs docker on a vagrant role
2. MySQL - this role setups a MySQL clusters (master and slaves)
3. redis - this role installs redis cluster
4. rabbitmq - this role installs rabbitmq cluster



Running the Ansible Playbook
===============================

An ansible playbook `playbook.yml` installs the necessary dependencies runs the various roles specified in the playbook . To execute the playbook on Vagrant, run:

The management console for RabbmitMQ can be accessed at http://172.30.1.5:15672

## Initialize Vagrant
```
vagrant up
```
