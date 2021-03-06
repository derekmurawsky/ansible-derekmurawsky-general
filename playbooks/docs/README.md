# Playbooks

The following playbooks are bundled with this collection.

!!! note
    All playbooks in this bundle target all hosts by default. You can target specific hosts by passing `-e 'target=hostname-or-group'` on the command line to override this behavior.

## bootstrap

A *very* simple playbook that will use the collections bootstrap role to bootstrap all targeted hosts for ansible management.

!!! warning

    This playbook will use the `~/.ssh/id_rsa.pub` key of the current user by default. You can also pass it a public key with `-e 'pubkey=....'`.

## host_facts

This is a handy and simple playbook that will dump out all the facts available on a host. Especially handy when you save the output to a file.

`ansible-playbook derekmurawsky.general.host_facts -l host > facts.txt`

## proxmox

A simple playbook that will apply the proxmox roles from this collection to all targeted hosts.
