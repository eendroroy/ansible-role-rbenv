rbenv
=========

[![Build Status](https://travis-ci.org/eendroroy/ansible-role-rbenv.svg?branch=master)](https://travis-ci.org/eendroroy/ansible-role-rbenv)

Ansible role to install rbenv

Role Variables
--------------

Set `env: system` to install rbenv system-wide, or `env: local` for local installation.

Add plugins under `plugins` var.

Define ruby versions to install under `rubies` var.

Example:

```yml
env: system
plugins:
  - { name: ruby-build, repo: 'https://github.com/rbenv/ruby-build.git' }

rubies:
  - version: 2.4.0
```

Supported OS
------------

- Ubuntu
    - precise (12.04)
    - saucy (13.10)
    - trusty (14.04)
    - xenial (16.04) - xenial requires python2 to be installed for ansible support

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: eendroroy.rbenv }

License
-------

MIT

Author Information
------------------

**Indrajit Roy** - *owner* - [eendroroy](https://github.com/eendroroy)
