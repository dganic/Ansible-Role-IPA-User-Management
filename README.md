ipa-user-management
=========

Ansible role for user management and group in FreeIPA

Supported platforms
------------

##### IPA, version: 4.9 and above

Role Variables
--------------

Please see a file: defaults/main.yml

You can also use tags: 

*  __user__ - only create users
*  __group__ - create group and add users to groups

Dependencies
------------

* None

Example Playbook
----------------

    - name: FreeIPA user management
      hosts: {{ ipa_server }}
      remote_user: "{{ lookup('env', 'LOGNAME') }}"
      gather_facts: false
      roles:
        - ipa-user-management
      vars:
        ipa_server: 172.31.104.24
        user_list: ./ipausers/users.yaml
        user_init_file: ./ipausers/created/

License
-------

MIT

Author Information
------------------

Aleksandr Anishchenko
