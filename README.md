# Ansible playbook collection by rkeri (CentOS 7)
version 0.3

## Contents
 - apache configuration playbook
 - wordpress configuration playbook
 - mariadb database configuration playbook (remote too)

## Requirements
 - CentOS 7 (other distros in plan)
 - Ansible (yum install epel-release / ansible)
 - your server addresses in ansible/hosts
 - ssh access to your servers / clients

## Apache
Requirements:
- sshd.conf:
  - passwordauth = yes
  - root privileges = yes

To run with keypairs, set sudo ssh password, and run with the following command: sudo ansible-playbook apacheconf.yml --vault-password-file=vault.txt

vault.txt -> your vault password (ansible-vault create "yourvaultfile")
 - ansible_sudo_pass: "mysudopassword"

## Wordpress
Installs and configures a fresh wordpress on your webserver with the prerequisities

## RemoteDB for wordpress
Installs and configures a MariaDB server with a preferred localhost and remote user with the prerequisities

## LAMP stack with Wordpress in a remote Database
Basically the Apache, Wordpress, and RemoteDB playbooks combined (recommended)

## LAMP stack with wordpress on localhost
Same as above, but with everything on localhost (only recommended if you have only one server)

## ToDo
LetsEncrypt SSL certificate generator with autorenew feature for safe and easy https access
