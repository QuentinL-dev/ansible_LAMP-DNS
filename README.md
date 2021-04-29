# LAMP-DNS Deployment with Ansible

## Generalities
Here is an ansible playbook allowing to easily deploy a LAMP server (Linux Apache MySQL PHP).
It also allows you to configure a DNS server to resolve the domain name of the new site created.

## Dependencies

#### ANSIBLE
This version has been tested with:
- ansible 2.9.20
- python version = 2.7.16 (default, Oct 10 2019, 22:02:15) [GCC 8.3.0]

## Parameters
In order to add your own parameters, please edit vars/vars.yml.
In addition, it is imperative to modify the hosts file by entering the IP address of your own remote host.

## To run the playbook:
    $ ansible-playbook -i hosts deploy.yml

