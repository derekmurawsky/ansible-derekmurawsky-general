# proxmox-nginx

A role that configures nginx as a reverse proxy on the proxmox server. It installs and configures nginx as a reverse proxy pointing to the proxmox server behind it. It utilizes ProxMox's default certificates.

## Requirements

None

## Role Variables

None - This uses the server's name in your ansible inventory as the FQDN for the nginx config.

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: proxmox_servers
  roles:
    - proxmox_nginx
  become: yes
```

## Useful links

- [Proxmox nginx documentation](https://pve.proxmox.com/wiki/Web_Interface_Via_Nginx_Proxy)
