# ansible_playbooks

Install ansible

    sudo apt-add-repository ppa:ansible/ansible &&
    sudo apt update && sudo apt install ansible -y

Set inventory file with hosts

    sudo vim /etc/ansible/hosts

    [servers]
    server1 ansible_host=203.0.113.111
    server2 ansible_host=203.0.113.112

    [all:vars]
    ansible_python_interpreter=/usr/bin/python3

Run playbook

	ansible-playbook -v playbook.yml -l fra1

## References

- https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-20-04
- https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-20-04
- https://gist.github.com/devster31/74e48cc1c8e73c637bc7
- https://github.com/do-community/ansible-playbooks
