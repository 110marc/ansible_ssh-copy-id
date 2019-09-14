ansible_ssh-copy-id
=========

Role is intended to copy an existing ssh public key `id_rsa.pub` to an existing `remote` user for ssh key pair authentication.

Requirements
------------

_Optional:_ Run it with sudo password prompt:
```
ansible-playbook --ask-become-pass main.yml -l remote
BECOME password: 
```

Role Variables
--------------

Existing `remote` user.

Dependencies
------------

If the user does not exist, it may require [`ansible_create_user`](https://github.com/110marc/ansible_create_user) role to be played prior `ansible_ssh-copy-id`

Example Playbook
----------------

An example of how to use your role:

    - hosts: servers
      become: yes
      roles:
         - ansible_create_user *optional
         - ansible_ssh-copy-id

License
-------

BSD

Author Information
------------------

> https://github.com/110marc
