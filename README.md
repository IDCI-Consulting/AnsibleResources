# AnsibleResources

This repo is used to install some packages into an remote host.

## Requirements

- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

### Remote host

The following requirements must be installed into the remote host :

- [Ubuntu](https://www.ubuntu.com/)
- [Openssh-server](https://help.ubuntu.com/lts/serverguide/openssh-server.html)
- [Python](https://wiki.ubuntu.com/Python)

_Note: Use [APT](https://help.ubuntu.com/lts/serverguide/apt.html) to install requirements_

## Configuration

You have to configure Ansible hosts in `/etc/ansible/hosts` :

```
[idcidev]
YOUR_HOSTNAME              ansible_ssh_host=YOUR_SSH_HOST ansible_ssh_user=YOUR_SSH_USER
```

## Installation

Run the following command to install packages into the remote host :

```sh
$ ansible-playbook config_dev.yml --ask-pass --ask-become
```
