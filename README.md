Ansible role: user-ssh-key
==========================

This ansible role add **new user** and **set authorized key**.
Sample task with role:

```yaml
# Create user with ssh
- name: Create user with ssh
  hosts: all
  become: true
  roles:
  - role: user-ssh-key
    username: che
    userkey: https://github.com/chernyshaw.keys
    userpasswd: 9ppIVeoX6jhCWfnc
    salt: somesalt
```