# Ansible Role: ROS

[![Build Status](https://travis-ci.org/pgorczak/ansible-role-ros.svg?branch=master)](https://travis-ci.org/pgorczak/ansible-role-ros)

Deploy ROS to an Ubuntu machine.

## Requirements

The role configures package sources and installs packages. You need to run it with root privileges.

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


## Use in production

* [Install from Ansible Galaxy](https://galaxy.ansible.com/pgorczak/ros).
* Remember that managed hosts need *python-simplejson* for playbook to work.
* Use the role like in the example playbook, but instead of *ansible-role-ros*, use **pgorczak.ros**.
* Make sure you have key-based access to a sudo user on the managed hosts.
* Tip: run *ansible-playbook* with `-u USERNAME` to specify the user and `-K` to allow it to ask for the sudo password.
