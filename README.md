[![Ansible Galaxy](https://img.shields.io/badge/galaxy-hugoprudente.envoyproxy-5bbdbf.svg)](https://galaxy.ansible.com/hugoprudente/envoyproxy)
[![Lint](https://github.com/hugoprudente/ansible-role-envoyproxy/actions/workflows/lint.yml/badge.svg?branch=main)](https://github.com/hugoprudente/ansible-role-envoyproxy/actions/workflows/lint.yml)
[![Molecule CI/CD](https://github.com/hugoprudente/ansible-role-envoyproxy/actions/workflows/integration.yml/badge.svg?branch=main)](https://github.com/hugoprudente/ansible-role-envoyproxy/actions/workflows/integration.yml)
[![License](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# Ansible Envoy Proxy Role

[Envoy Proxy](envoyproxy.io) it's a powerful edge and service proxy developed for Cloud Native applications. It's a gratuated project in the [CNCF](https://www.cncf.io/projects/) and has native integrations with [Jagger](https://www.jaegertracing.io/) for observability, [Prometheus](https://prometheus.io/) for metrics and insights and others.

This role goal is to help users to deploy and configure the basic of the Envoy Proxy, to a VM and baremetal as alternative for the conventional Proxies, Load Balancers tools. 

Envoy Proxy configurations will **NOT** be covered here as they have a extra level of complexity that will require a Ansible Collections / Module.

## Requirements

### Ansible

* This role is developed and tested with [maintained](https://docs.ansible.com/ansible/latest/reference_appendices/release_and_maintenance.html#release-status)
  versions of Ansible. Backwards compatibility is not guaranteed.
* Instructions on how to install Ansible can be found in the [Ansible website](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

### Molecule

* Molecule `3.x` is used to test the various functionalities of the role.
* Instructions on how to install Molecule can be found in the [Molecule website](https://molecule.readthedocs.io/en/latest/installation.html).

### Ansible Galaxy

Use `ansible-galaxy install hugoprudente.envoyproxy` to install the latest stable release of the role on your system.

### Git

Use `git clone https://github.com/hugoprudente/ansible-role-envoyproxy.git hugoprudente.envoyproxy` inside your **roles/** 
directory to pull the latest edge commit of the role from GitHub.

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
- focal (20.04)
Debian:
- duster (10)
```

## Role Variables

This role has multiple variables. The descriptions and defaults for all these variables can be found in the **[`defaults/main/`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/)** folder in the following files:

|Name|Description|
|----|-----------|
|**[`main.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/main.yml)**|Envoy Proxy installation variables|
|**[`systemd.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/systemd.yml)**|Systemd installation variables|
|**[`logrotate.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/logrotate.yml)**|Logrotate installation variables|
|**[`cluster.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/defaults/main/cluster.yml)**|Cluster installation variables|

Similarly, descriptions and defaults for preset variables can be found in the **[`vars/`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/vars/)** folder in the following files:

|Name|Description|
|----|-----------|
|**[`main.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/vars/main.yml)**|List of supported Envoy Proxy platforms and modules|

## Example Playbooks

Working functional playbook examples can be found in the **[`molecule/`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/)** folder in the following files:

|Name|Description|
|----|-----------|
|**default/[`converge.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/default/converge.yml)**|Install a default version of Envoy Proxy|
|**container/[`converge.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/container/converge.yml)**|Install a containerised version of Envoy Proxy|
|**source/[`converge.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/source/converge.yml)**|Install Envoy Proxy building from the source|
|**cluster/[`converge.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/cluster/converge.yml)**|Install clustered version of Envoy Proxy (Primary/Primary) and (Active/Backup)|
|**custom/[`converge.yml`](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/molecule/custom/converge.yml)**|Install a specific of Envoy Proxy add log rotate and systemd custom|

## License

[Apache License, Version 2.0](https://github.com/hugoprudente/ansible-role-envoyproxy/blob/main/LICENSE)

## Author Information

[Hugo Prudente](https://github.com/hugoprudente/)
