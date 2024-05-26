Timeshift
=========

Installs and configures [timeshift](https://github.com/linuxmint/timeshift) for the user.

Requirements
-----------------

This role has no requirements.
To include this role in your `requirements.yml` file, add the following list item:

```yaml
---
roles:
  - name: whalej84.timeshift
    src: https://github.com/WhaleJ84/ansible-role-timeshift.git
    scm: git
```

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
