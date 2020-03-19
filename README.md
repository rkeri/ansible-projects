# Ansible playbook collection by rkeri (CentOS 7)
version 0.3

## Contents
 - apache configuration playbook
 - wordpress configuration playbook
 - mariadb database configuration playbook (remote too)

## Requirements
 - CentOS 7 (other distros in plan)
 - Ansible (yum install epel-release / ansible)
 - your server addresses in ansible/hosts with ip and login credentials (e.g. ansible_host="yourhostip" ansible_user="hostuser" ansible_ssh_pass="hostpassword")
 - ssh access to your servers / clients
 - sshd.conf:
   - passwordauth = yes
   - root privileges = yes

To run with keypairs, set sudo ssh password, and run with the following command: sudo ansible-playbook apacheconf.yml --vault-password-file=vault.txt

vault.txt -> your vault password (ansible-vault create "yourvaultfile")
 - ansible_sudo_pass: "mysudopassword"   

## Apache
Installs apache with prerequisities, adds firewall rules, configurable virtualhost, and a sample index.html

## Wordpress
Installs and configures a fresh wordpress on your webserver with the prerequisities

## RemoteDB for wordpress
Installs and configures a MariaDB server with a preferred localhost and remote user with the prerequisities

## GetDocker
Downloads / tests docker

## certbot-d
Generates an SSL certificate with autorenew feature using certbot

## OTRS-ce
Downloads & configures an OTRS community edition with option for remote db
