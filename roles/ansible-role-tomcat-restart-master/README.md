# **Ansible Role: Tomcat Restart**

[![Build Status](https://travis-ci.org/thiagomgo/ansible-role-tomcat-restart.svg?branch=master)](https://travis-ci.org/thiagomgo/ansible-role-tomcat-restart) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-tomcat--restart-blue.svg)](https://galaxy.ansible.com/thiagomgo/tomcat-restart/)

This role is used to restart a tomcat service.

## Requirements

This role only requires Ansible version 1.8+.

## Role Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---

# Tomcat info
tomcat_path: /opt/tomcat # (required)
tomcat_port: 8080        # (required)

```

## Dependencies

None

## Example Playbook

```yaml
---

- hosts: all

  vars:
    tomcat_path: /opt/tomcat
    tomcat_port: 8080

  roles:
    - { role: ansible-role-deploy-java, tags: [ 'stop', 'start' ] }

```

## License

MIT / BSD

## Author Information

Thiago Gomes
- thiago.mgomes [at] gmail.com

