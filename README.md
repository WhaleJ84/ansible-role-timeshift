Timeshift
=========

Installs and configures [timeshift](https://github.com/linuxmint/timeshift) for the user.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

This example playbook shows how I would use this role, with custom variables to suit my needs.

```yaml
- hosts: localhost

  roles:
    - role: whalej84.timeshift
      vars:
        remove_gui_password_prompt: "true"
        location_mount: "/"
        do_first_run: "false"
        schedule_monthly: "true"
        schedule_weekly: "true"
        schedule_daily: "true"
        schedule_boot: "true"
        include_btrfs_home_for_backup: "true"
        include_btrfs_home_for_restore: "true"
      tags: [ timeshift ]
```
