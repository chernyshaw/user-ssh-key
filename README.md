Ansible role: user-ssh-key
==========================

This ansible role add **new user** and **set authorized key**.
Sample task with role:

```yaml
- name: Create user with ssh
  hosts: all
  become: true
  roles:
  - role: user-ssh-key
    username: che
    userkey: https://github.com/chernyshaw.keys
    userpasswd: Qwerty123
    salt: somesalt
```
