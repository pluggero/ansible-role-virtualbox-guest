# Ansible Role: VirtualBox Guest Additions

[![CI](https://github.com/pluggero/ansible-role-virtualbox-guest/actions/workflows/ci.yml/badge.svg)](https://github.com/pluggero/ansible-role-virtualbox-guest/actions/workflows/ci.yml) [![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/pluggero/virtualbox_guest?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/pluggero/virtualbox_guest)

An Ansible Role that installs VirtualBox Guest Additions on Linux distributions and FreeBSD.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
virtualbox_guest_version: "x.x"
```

The version of Virtualbox Guest Additions to install can be defined in the variable `virtualbox_guest_version`.

```yaml
virtualbox_guest_install_method: "source"
```

The method used to install virtualbox_guest can be defined in the variable `virtualbox_guest_install_method`.
The following methods are available:

- `source`: Installs VirtualBox Guest Additions from source
- `package`: Installs VirtualBox Guest Additions from OS native packages

```yaml
virtualbox_guest_reboot: true
```

Defines if the system should be rebooted in the installation process of VirtualBox Guest Additions.
This should be false if you install it in a special environment like with packer.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - pluggero.virtualbox_guest
```

## License

MIT / BSD

## Author Information

This role was created in 2025 by Robin Plugge.
