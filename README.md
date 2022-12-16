Role Name
=========

[![.github/workflows/test.yml](https://github.com/airdata/ansible-role-yaml-validation/actions/workflows/test.yml/badge.svg)](https://github.com/airdata/ansible-role-yaml-validation/actions/workflows/test.yml)

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| VariableName              	| Default Value                            	|        	| Mandatory 	|
|---------------------------	|------------------------------------------	|--------	|-----------	|
| env                       	| dev                                      	| String 	| yes       	|
| templates_folder_yaml     	| templates/                               	| String 	| yes       	|
| templates_folder_yamllint 	| templates/                               	| String 	| yes       	|
| yamllint_config           	| - yamllint-a.yml<br>- yamllint-b.yml     	| List   	| Y         	|
| yaml_files                	| - example-a.yml.j2<br>- example-b.yml.j2 	| List   	| Y         	|
-----------------------------------------------------------------------------

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      vars:
        yaml_files:
          - files/example.yml.j2
          - files/some_oher_file.yml.j2
        env: dev
      roles:
          - ansible-role-yaml-validation

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
