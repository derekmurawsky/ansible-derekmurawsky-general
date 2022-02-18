# derekmurawsky.general ansible collection

This collection contains some roles and playbooks that I use to set up and maintain my homelab. An overview of the playbooks and roles is below, with more details in the relevant documentation sections.

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

## Development

The easiest way to work with this project is to git clone it and then open it with VSCode. This is a devcontainer enabled repo. Once the devcontainer is built once, it will run much faster in the future.

### To build and test locally

1. Create a `requirements.yml` that points to this module's directory.

```yaml
---
collections:
  - source: derekmurawsky/general
    type: dir
```

2. Install the collection by running the command `ansible-galaxy collection install -r requirements.yml --force`.
3. Any time you make a change to the code that you want to test, you must re-run the command from step 2

<!-- markdownlint-disable-file MD029 -->