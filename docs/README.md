# derekmurawsky.general ansible collection

This collection contains some roles and playbooks that I use to set up and maintain my homelab. An overview of the playbooks and roles is below, with more details in the relevant documentation sections.

## Playbooks

All playbooks in this bundle target all hosts by default. You can target specific hosts by passing `-e 'target=hostname-or-group'` on the command line to override this behaviour.

### Bootstrap

A *very* simple playbook that will use the collections bootstrap role to bootstap all targetted hosts for ansible management.

### Proxmox

A simple playbook that will apply the proxmox roles from this collection to all targetted hosts.

## Roles

### ansible_bootstrap

A role to help bootstrap a linux server for ansible management. It provisions a user, adds the user to the sudoers group, and configures passwordless sudo for that user.

### proxmox_base

A role that does some baseline configuration on a proxmox server. It adds the pve-no-subscription repo, updates the cache, and puts vmbr0 vlan-aware.

### proxmox_nginx

A role that configures nginx as a reverse proxy on the proxmox server. It installs and configures nginx as a reverse proxy pointing to the proxmox server behind it. It utilizes ProxMox's default certificates.
