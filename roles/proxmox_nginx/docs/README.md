# proxmox-nginx

A role that configures nginx as a reverse proxy on the proxmox server. It installs and configures nginx as a reverse proxy pointing to the proxmox server behind it. It utilizes ProxMox's default certificates.

## Requirements

None

## Role Variables

| Variable                          | Default                    | Description                        |
| --------------------------------- | -------------------------- | ---------------------------------- |
| proxmox_nginx_ssl_certificate     | /etc/pve/local/pve-ssl.pem | Path to the server certificate     |
| proxmox_nginx_ssl_certificate_key | /etc/pve/local/pve-ssl.key | Path to the server certificate key |

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
