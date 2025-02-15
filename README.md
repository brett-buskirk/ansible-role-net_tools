# ansible-role-net_tools

This Ansible role installs common networking diagnostic tools on Ubuntu-based systems.

## Requirements

* An Ubuntu-based system.
* Ansible version 2.9 or later.
* Root privileges (via `become: true`).

## Role Variables

This role does not use any variables.

## Dependencies

This role has no dependencies.

## Example Playbook

```yaml
- hosts: your_hosts
  become: true
  roles:
    - brett-buskirk.net_tools
```

## Installation

You can install this role using Ansible Galaxy:

```bash
ansible-galaxy install brett-buskirk.net_tools
```

Or you can include it in your `requirements.yml` file:

```yaml
---
roles:
  - name: brett-buskirk.net_tools
    src: [https://github.com/brett-buskirk/ansible-role-net_tools](https://www.google.com/search?q=https://github.com/brett-buskirk/ansible-role-net_tools)
    version: main # or a specific tag
```

Then install it using:

```bash
ansible-galaxy install -r requirements.yml
```

## Role Tasks

This role performs the following tasks:

* **Update apt cache:** Updates the apt package cache to ensure the latest package information is available.
* **Install networking diagnostic tools:** Installs the following packages:
  * `net-tools`: Provides basic networking utilities like `ifconfig` and `netstat`.
  * `traceroute`: Traces the route packets take to a network host.
  * `nmap`: A powerful network scanner and security auditing tool.
  * `iproute2`: Provides advanced networking utilities like `ip`.

## Usage

Include the role in your playbook as shown in the "Example Playbook" section. The role will automatically install the necessary packages on the target host.

## License

MIT

## Author Information

This role was created by Brett Buskirk for RC Journey.

## Galaxy Tags

```
networking, network, tools, diagnostics, net-tools, traceroute, netcat, iproute2, system, utility, admin
```
