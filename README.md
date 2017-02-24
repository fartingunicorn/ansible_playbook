# Ansible provisioning out of a docker container

`docker pull madhub/ansible_playbook`

## Examples

### run playbook
`docker run --rm -it -v $(pwd):/ansible/playbooks madhub/ansible_playbook -i inventory/ secure-server-pl.yml -k -u root`

### run playbook with ssh-key auth
`docker run --rm -it --volumes-from keystore -v $(pwd):/ansible/playbooks madhub/ansible_playbook -i inventory/ install-application.yml --ask-become-pass -u deploy`

## Ansible Dokumentation
* http://docs.ansible.com/ansible/playbooks_best_practices.html
* https://www.ansible.com/blog/ansible-best-practices-essentials

## Howto ssh-key gen
Create a ssh-key out of a docker container. Please refer to my other repo.
* https://github.com/fartingunicorn/ssh-keygen
* https://hub.docker.com/r/madhub/ssh-keygen
