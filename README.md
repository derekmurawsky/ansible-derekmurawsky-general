# Ansible Collection - derekmurawsky.general

This collection contains some roles and playbooks that I use to set up and maintain my homelab.

## Documentation

Documentation is available at [https://derekmurawsky.github.io/ansible-derekmurawsky-general/](https://derekmurawsky.github.io/ansible-derekmurawsky-general/).

This collection is documented using [MKDocs](https://www.mkdocs.org/) with the [Material](https://squidfunk.github.io/mkdocs-material/) theme and the [MKDocs Monorepo](https://github.com/backstage/mkdocs-monorepo-plugin) plugin.

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