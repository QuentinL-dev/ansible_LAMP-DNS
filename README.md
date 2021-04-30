# LAMP-DNS Deployment with Ansible

## Generalities
Here is an ansible playbook allowing to easily deploy a LAMP server (Linux Apache MySQL PHP) and to configure a DNS server to resolve the domain name of the new site created.

In addition, the second playbook (deploy-tomcat.yml) adds Apache Tomcat to the LAMP server.

## Dependencies

### ANSIBLE
This version has been tested with:
- ansible 2.9.20
- python version = 2.7.16 (default, Oct 10 2019, 22:02:15) [GCC 8.3.0]

To easily install ansible on Debian, please run the following commands as root:
```console
$ cd ansible-installation
$ ./debian.install-ansible.sh
```

### REMOTE HOST OS
Since this playbook uses the apt module, the remote host must have a Debian-like os.
This version has been tested with:
- Ubuntu Desktop 20.04 LTS
- Debian 10 Buster

## Parameters and Settings
In order to add your own parameters, please edit vars/vars.yml.
In addition, it is imperative to modify the hosts file by entering the IP address of your own remote host.

## To run the playbook
- LAMP-DNS installation:
```console
$ ansible-playbook -i hosts deploy.yml
```

- Apache Tomcat installation:
```console
$ ansible-playbook -i hosts deploy-tomcat.yml
```

## Troubleshootings
In order to avoid any errors concerning the configuration of MySQL - in particular the creation of users - MySQL must not have been installed beforehand on the remote host.
