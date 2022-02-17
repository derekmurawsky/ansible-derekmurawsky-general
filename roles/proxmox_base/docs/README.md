# Proxmox base

A simple role that does some baseline configuration on a proxmox server. It adds the pve-no-subscription repo, updates the cache, and puts vmbr0 vlan-aware.

## Requirements

None

## Role Variables

| Variable                            | Default | Description                                     |
| ----------------------------------- | ------- | ----------------------------------------------- |
| proxmox_install_pve_no_subscription | true    | If true, installs the pve_no_subscription repo. |

## Dependencies

- community.general

## Example Playbook

```yaml
---
- hosts: proxmox_servers
  roles:
    - proxmox_base
  become: yes
```
