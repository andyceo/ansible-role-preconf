# Ansible Role: preconf

This role supposed to execute first and it checks that all packages are updated and make some adjustments to sysctl.

## Requirements

Ubuntu 16.04


## Tags:

- **preconf-apt-keys**: only add/remove keys to/from apt keyring (use `preconf.apt_keys` configuration variable)
- **preconf-apt-repositories**: only add/remove repositories to/from apt (use `preconf.repositories` configuration variable)
