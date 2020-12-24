Ansible Role: Packer
====================

[![CI](https://github.com/zubkovdv/ansible-role-packer/workflows/CI/badge.svg?event=push)](https://github.com/zubkovdv/ansible-role-packer/actions?query=workflow%3ACI)

Automatically finds and installs the latest version of [HashiCorp Packer](https://www.packer.io) on RHEL/CentOS and Debian/Ubuntu servers.

Requirements
------------

None.

Role Variables
--------------

Default values are listed below (see `defaults/main.yml`):  

`packer_version: "1.6.2"`  
The variable is commented out **(default)** - the latest version of the package will be automatically found and installed. In this case, **the pip package `github3.py` will be installed** on the Ansible Master host.  
The variable is not commented out - the specified version of the package will be installed.

`packer_arch: "amd64"`  
The system architecture to use: `amd64`**(default)** or `386`.

`packer_bin_path: /usr/local/bin`  
The location where the Packer binary package will be installed.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - zubkovdv.packer

License
-------

MIT

Author Information
------------------

This role was created by Dmitry Zubkov.
