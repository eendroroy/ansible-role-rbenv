# rbenv

[![Build Status](https://travis-ci.org/eendroroy/ansible-role-rbenv.svg?branch=master)](https://travis-ci.org/eendroroy/ansible-role-rbenv)

[![Contributors](https://img.shields.io/github/contributors/eendroroy/ansible-role-rbenv.svg)](https://github.com/eendroroy/ansible-role-rbenv/graphs/contributors)
[![GitHub last commit (branch)](https://img.shields.io/github/last-commit/eendroroy/ansible-role-rbenv/master.svg)](https://github.com/eendroroy/ansible-role-rbenv)
[![license](https://img.shields.io/github/license/eendroroy/ansible-role-rbenv.svg)](https://github.com/eendroroy/ansible-role-rbenv/blob/master/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/eendroroy/ansible-role-rbenv.svg)](https://github.com/eendroroy/ansible-role-rbenv/issues)
[![GitHub closed issues](https://img.shields.io/github/issues-closed/eendroroy/ansible-role-rbenv.svg)](https://github.com/eendroroy/ansible-role-rbenv/issues?q=is%3Aissue+is%3Aclosed)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/eendroroy/ansible-role-rbenv.svg)](https://github.com/eendroroy/ansible-role-rbenv/pulls)
[![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/eendroroy/ansible-role-rbenv.svg)](https://github.com/eendroroy/ansible-role-rbenv/pulls?q=is%3Apr+is%3Aclosed)

Ansible role to install rbenv

## Role Variables

Set `rbenv_env: system` to install rbenv system-wide, or `rbenv_env: local` for local installation.

Add plugins under `rbenv.plugins` var.

Define ruby versions to install under `rubies` var.

Example:

```yml
rbenv_env: system

rbenv:
  plugins:
    - { name: ruby-default-gems, repo: 'https://github.com/rbenv/ruby-default-gems.git' }

rubies:
  - version: 2.5.0
```

## Supported OS

- Ubuntu
    - trusty  (14.04)
    - xenial  (16.04) - xenial requires python2 to be installed for ansible support
- CentOS
    - 7
- RHEL
    - 7

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: eendroroy.rbenv, rbenv_env: system }


## Testing locally

First run the vagrant machines:

```bash
vagrant up
```

Then execute the test runner script:

```bash
./run_vagrant_test.sh
```

## Contributing

Bug reports and pull requests are welcome on GitHub at [ansible-role-rbenv](https://github.com/eendroroy/ansible-role-rbenv) repository.
This project is intended to be a safe, welcoming space for collaboration,
and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Authors

* **Indrajit Roy** - *Owner* - [eendroroy](https://github.com/eendroroy)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
