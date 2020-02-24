# ansible-projects
version 0.1

## contents
 - apache configuration playbook
 - wordpress configuration playbook
 - tbd

## Apache
Requirements:
- sshd.conf -> passwordauth = yes
            -> root privileges = yes

to run with keypairs, set sudo ssh password, and run with the following command: sudo ansible-playbook apacheconf.yml --vault-password-file=vault.txt

vault.txt -> your vault password (ansible-vault create "yourvaultfile"):
  ansible_sudo_pass: "mysudopassword"

## Wordpress
-ToDo

## RemoteDB for wordpress
-ToDo
