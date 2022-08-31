Role Name : docker-install
=========
This role install docker-ce, docker-ce-cli and python3 dependencies for control docker with python.
```
@all:
  |--@dev:
  |  |--192.168.56.3
  |  |--192.168.56.4
  |--@prod:
  |  |--192.168.56.13
  |  |--192.168.56.14
  |  |--192.168.56.16
  |--@stage:
  |  |--192.168.56.23
  |  |--192.168.56.24
  |  |--192.168.56.6
  |--@ungrouped:
```
Requirements
------------


Role Variables
--------------
```
Global variables specific to different development environments are stored in inventory directory ~/.ansible/inventory/.
      inventory/
      ├── dev
      │   └── hosts.yaml
      ├── group_vars
      │   ├── dev
      │   │   ├── vars.yaml
      │   │   └── vault.yaml
      │   ├── prod
      │   └── stage
      ├── prod
      │   └── hosts.yaml
      └── stage
          └── hosts.yaml
```
Variables for current role stored in ./vars/ and ./defaults/

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: dev
      roles:
        - docker-install
        #- { role: username.rolename, x: 42 }


$ ansible-playbook --vault-password-file .vault-pass.dev docker_install.yaml

License
-------

BSD

Author Information
------------------
Nik 

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
