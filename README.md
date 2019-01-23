# Ansible Role: ROS

[![Build Status](https://travis-ci.org/pgorczak/ansible-role-ros.svg?branch=master)](https://travis-ci.org/pgorczak/ansible-role-ros)

Deploy ROS to an Ubuntu machine.

## Requirements
Note that the simplejson package must be available on remote machines

    pip install python-simplejson


## Role Variables

* **ros_packages**: A list of ros packages to install (sans the `ros-dist-`
  prefix).


## Test Locally
To setup a VM for each supported Ubuntu release with `ros-base`, run

    vagrant up

The Vagrant configuration uses a simple [example playbook](./example.yml),
setting up ROS like

```yaml
roles:
- { role: ansible-role-ros, ros_packages: ['ros-base', 'urdfdom-py'] }
```
