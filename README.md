## ansible-docker_centos
=========

Ansible role build by me to:

- Provision two CentOS hosts locally (created by Vagrant)
- Install Docker (ce edition)
- Install Docker-Compose using PIP
- Add 'vagrant' user to the 'docker' group so you can use docker without root permission


------------

- I used an Ubuntu 20.04 LTS (Focal Fossa) control node, in which i installed ansible 2.9
- Vagrant to create the virtual machines locally
- Virtualbox as a provider for Vagrant

## Example Playbook
```
---

#playbook.yml

- name: Example playbook
  hosts: all
  become: true

  roles:
    - role: "anto.docker_centos"

```
To use the playbook: `ansible-playbook playbook.yml`
----------

## Vagrant setup
- In order to create the virtual machines, i used vagrant
- The Vagrantfile configuration is available in this repository

I used 'bento/centos-7' base box for both the VMs. I also used a 2GB memory for each host and set a private network ip address.
``` 
vb.memory = 2048 

vm1.vm.network "private_network", ip: "192.x.x.x"
```

As mentioned before, i used Virtualbox as a provider






