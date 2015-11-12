# homebrew

Mac OS X Homebrew manager


## Role Variables
```yml
---
  homebrew_packages:
    - name: dos2unix
      state: present
      upgrade_all: false
      update_homebrew: false
      install_options: enable-debug
    - name:
```


Example Playbook
----------------
```yml
---
- hosts: local
  sudo: true
  gather_facts: true

  roles:
    - marcelocorreia.serf-install

  vars_files:
    - ../vars/tardis.yml
```

License
-------

MIT

Author Information
------------------
Some useful stuff at:
  - [https://github.com/marcelocorreia](https://github.com/marcelocorreia)
  - [https://galaxy.ansible.com/list#/users/15516](https://galaxy.ansible.com/list#/users/15516)
  - [https://hub.docker.com/u/marcelocorreia/](https://hub.docker.com/u/marcelocorreia/)
  - Any issues, pull-request are welcome
