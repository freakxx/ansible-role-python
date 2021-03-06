# Ansible Role: Python

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-python.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-python)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-fubarhouse--python-5140.svg)](https://galaxy.ansible.com/fubarhouse/python)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/fubarhouse/ansible-role-hub/master/LICENSE)

* PyEnv on Darwin/Debian/RedHat servers.
* Installs multiple python versions as required.
* Installs a virtualenv for a specified version of Python.
* Installs PIP packages

## Requirements

  None.

## Role Variables

Default Python version
````
python_version: 2.7.11
````
All Python versions to install
````
python_versions:
- 2.7.11
- 3.5.1
````
Python packages to download
````
python_packages:
- pyyaml
- jinja2
- virtualenv
- pyasn1
- Django
````
List of all virtualenvs to install

**Note**: If this is not specified, the variable `python_version` will be allocated to this array.
````
virtualenvs:
- name: "Global-2.7.11"
  version: 2.7.11
````
Virtualenvs to use as the global python system

**Note**: If this is not specified, the variable `python_version` will be allocated to this variable.
````
virtualenv: 2.7.11
````
## Dependencies

None.

## Example Playbook
````
- hosts: localhost
  roles:
    - fubarhouse.python
````

## Installation

* Install using `ansible-galaxy install fubarhouse.python`
* Add the Python role to your playbook.
* Modify above variables as desired.

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Karl Hepworth](https://twitter.com/fubarhouse).
