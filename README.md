# Ansible Envoy Proxy Role

A brief description of the role goes here.

## Requirements

### Ansible

* This role is developed and tested with [maintained](https://docs.ansible.com/ansible/latest/reference_appendices/release_and_maintenance.html#release-status)
  versions of Ansible. Backwards compatibility is not guaranteed.
* Instructions on how to install Ansible can be found in the [Ansible website](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

### Molecule

* Molecule `3.x` is used to test the various functionalities of the role.
* Instructions on how to install Molecule can be found in the [Molecule website](https://molecule.readthedocs.io/en/latest/installation.html).

### Ansible Galaxy

Use `ansible-galaxy install hugoprudente.` to install the latest stable release
of the role on your system.

### Git

Use `git clone https://github.com/hugoprudente/ansible-role-envoyproxy.git` to 
pull the latest edge commit of the role from GitHub.

## Platforms

Envoy Proxy role supports 

### Envoy Proxy

The Envoy Proxy role is working towards support all platforms supported by
[Envoy Proxy](https://www.envoyproxy.io/docs/envoy/latest/start/install).

At the moment I have tested it for:

```yaml
CentOS:
- 8
Ubuntu:
- focal
```


## Role Variables

This role has multiple variables. The descriptions and defaults for all these variables can be found in the **[`defaults/main/`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/)** folder in the following files:

|Name|Description|
|----|-----------|
|**[`main.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/main.yml)**|Envoy Proxy installation variables|


Similarly, descriptions and defaults for preset variables can be found in the **[`vars/`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/vars/)** folder in the following files:

|Name|Description|
|----|-----------|
|**[`main.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/vars/main.yml)**|List of supported Envoy Proxy platforms and modules|

## Example Playbooks

Working functional playbook examples can be found in the **[`molecule/common/playbooks/`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/common/playbooks/)** folder in the following files:

|Name|Description|
|----|-----------|
|**[`default_converge.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/common/playbooks/default_converge.yml)**|Install a specific version of Envoy Proxy|

Do note that if you install this repository via Ansible Galaxy, you will have to replace the role variable in the sample playbooks from `ansible-role-envoyproxy` to `hugoprudente.envoyproxy`.

## License

[Apache License, Version 2.0](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/LICENSE)

## Author Information

[Hugo Prudente](https://https://github.com/hugoprudente/)
