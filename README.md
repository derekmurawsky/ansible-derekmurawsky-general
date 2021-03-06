# Ansible Collection - derekmurawsky.general

[![CI](https://github.com/derekmurawsky/ansible-derekmurawsky-general/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/derekmurawsky/ansible-derekmurawsky-general/actions/workflows/ci.yml)

This collection contains some roles and playbooks that I use to set up and maintain my homelab. It is published to the [Ansible Galaxy](https://galaxy.ansible.com/derekmurawsky/general). More detailed documentation is available on the project's [github page](https://derekmurawsky.github.io/ansible-derekmurawsky-general/).

## Playbooks

All playbooks in this bundle target all hosts by default. You can target specific hosts by passing `-e 'target=hostname-or-group'` on the command line to override this behavior.

### Bootstrap

A *very* simple playbook that will use the collections bootstrap role to bootstrap all targeted hosts for ansible management.

### Proxmox

A simple playbook that will apply the proxmox roles from this collection to all targeted hosts.

## Roles

### ansible_bootstrap

A role to help bootstrap a linux server for ansible management. It provisions a user, adds the user to the sudoers group, and configures password-less sudo for that user.

### proxmox_base

A role that does some baseline configuration on a proxmox server. It adds the pve-no-subscription repo, updates the cache, and puts vmbr0 vlan-aware.

### proxmox_nginx

A role that configures nginx as a reverse proxy on the proxmox server. It installs and configures nginx as a reverse proxy pointing to the proxmox server behind it. It utilizes ProxMox's default certificates.
