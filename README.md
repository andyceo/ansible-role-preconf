# Ansible Role: preconf

This role supposed to execute first and it checks that all packages are updated and make some adjustments to sysctl.


## Requirements

Ubuntu 16.04 or
Ubuntu 18.04

## Configuration

Configuration can be made with one variable: `preconf`, that should be a dictionary. All configuration is organized in sections, which usualy maps to tags. For example, `preconf.apt_keys` section store apt keys and them can be executed with tag `preconf-apt-keys`.


## Tags:

- **preconf-apt-packages-remove**: remove or purge packages (use `preconf.packages_remove` configuration variable)
- **preconf-apt-keys**: only add/remove keys to/from apt keyring (use `preconf.apt_keys` configuration variable)
- **preconf-apt-repositories**: only add/remove repositories to/from apt (use `preconf.repositories` configuration variable)
- **preconf-apt-packages**: only install package sets declared in `preconf.package_sets_install` configuration variable. The package sets itself are declared in `preconf.package_sets` configuration variable.
- **preconf-apt**: process all apt-related tags: preconf-apt-packages-remove, preconf-apt-keys, preconf-apt-repositories, preconf-apt-packages
- **preconf-grub**: update Grub2 settings (for now it just set `GRUB_TIMEOUT` and `GRUB_RECORDFAIL_TIMEOUT` to `2` only and explicitly)
- **preconf-hostname**: only change node's hostname and /etc/hosts file respectively.
