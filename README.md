# Ansible role: user-ssh-key

This ansible role add **new user** and **set authorized key**.

#### Example Playbook

```yaml
- name: Create user with ssh
  hosts: all
  become: true
  roles:
  - role: user-ssh-key
```

#### Example inventory

```yaml
all:
  hosts:
    children:
       inv_name:
          ansible_host:
          vars:
            username: che
            userkey: https://github.com/chernyshaw.keys
            userpasswd: Qwerty123
            salt: somesalt
```