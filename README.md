# Ansible Role: vector

[v1.0.1](https://github.com/Adel-pro/vector-role/tags)

## Description

Deploy Vector using Ansible.

## Requirements

- Ansible >= 2.10 (It might work on previous versions, but we cannot guarantee it)

- ## Role Variables

- All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |  
| -------------- | ------------- | -----------------------------------|  
| `version` | 0.34.2 | Vector version |  
| `arch` | amd64 | Processor architecture. It accepts the values "amd64", "arm64" or "armhf". |  
| `add_vector_docker_group` | no | If you want to add vector user to "docker" group, then put "yes". |  
| `add_vector_journal_group` | no | If you want to add vector user to "systemd-journal" group, then put "yes". |  

## Example

### Playbook

```yaml
---
- hosts: all
  roles:
  - vector
  vars:
    version: 0.9.2
    arch: arm64
```
