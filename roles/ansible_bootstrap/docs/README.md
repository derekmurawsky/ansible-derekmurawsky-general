# Ansible_Bootstrap

A simple role to help bootstrap a linux server for ansible management. It provisions a user, adds the user to the sudoers group, and configures password-less sudo for that user.

## Requirements

This role only requires a working ansible installation. However, the workflow can benefit from having the SSH askpass installed. See the example playbook below for why.

## Role Variables

| Variable                  | Default   | Description                                     |
| ------------------------- | --------- | ----------------------------------------------- |
| bootstrap_user_name       | ansible   | The username for ansible to provision           |
| bootstrap_user_shell      | /bin/bash | The shell for the user                          |
| bootstrap_user_ssh_pubkey | ""        | The ssh public key string to assign to the user |
| bootstrap_user_sudo_group | sudo      | The sudo group to add the user to               |

## Dependencies

This role uses only builtin modules.

## Example Playbook

Below is a simple playbook that can be called with any inventory to bootstrap a server with the public key of your current user. An example command would be `ansible-playbook -i hosts.yaml --ask-pass bootstrap.yaml`

```yaml
---
- hosts: all
  vars:
    bootstrap_user_ssh_pubkey: "{{ lookup('file', '~/.ssh/id_rsa.pub') }}"
  roles:
    - ansible_bootstrap
```
