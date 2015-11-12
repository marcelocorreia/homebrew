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
  - name: nginx
    state: absent
  - name: p7zip
    state: present
```


Example Playbook
----------------
```yml
---
- hosts:
    - local
  gather_facts: true

  roles:
    - { role: marcelocorreia.homebrew, tags: ['install','homebrew'], when: "ansible_system == 'Darwin'"}

  vars:
    homebrew_packages:
      - name: dos2unix
        state: present
        upgrade_all: false
        update_homebrew: false
        install_options: enable-debug
      - name: emacs
        state: absent
      - name: p7zip
        state: present
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
