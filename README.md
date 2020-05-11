# This Role Has Been Deprecated: Please use the version in the [oasis_roles.system](https://github.com/oasis-roles/ansible_collection_system) Ansible Collection

[![Build Status](https://travis-ci.com/oasis-roles/timezone.svg?branch=master)](https://travis-ci.com/oasis-roles/timezone)

timezone
===========

Sets the timezone information for the system

Requirements
------------

Ansible 2.8 or higher

Role Variables
--------------

Currently the following variables are supported:

### General

* `timezone` - Default: `null`. The name of the timezone to set the system
  to. For example, `timezone: America/Chicago`. Note, at least one of this or
  `timezone_hwclock` is required.
* `timezone_hwclock` - Default: `null`. Indicates whether the hardware clock
  is set to local time or UTC. Note, at least one of this or `timezone` is
  required.
* `timezone_become` - Default: true. If this role needs administrator
  privileges, then use the Ansible become functionality (based off sudo).
* `timezone_become_user` - Default: root. If the role uses the become
  functionality for privilege escalation, then this is the name of the target
  user to change to.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: timezone-servers
  roles:
    - role: oasis_roles.timezone
      timezone: Africa/Accra
```

License
-------

GPLv3

Author Information
------------------

Greg Hellings <greg.hellings@gmail.com>
