[![Build Status](https://travis-ci.org/misurellig/ansible_role_awsenv.svg?branch=master)](https://travis-ci.org/misurellig/ansible_role_awsenv)

ansible_role_awsenv
=========

Set up [awsenv](https://github.com/mauromedda/awsenv) utility.


Requirements
------------

The role has been tested on the following stack:

  * CentOS 7

Dependencies
------------


Role Variables
--------------

| parameter               | required | default                                                          |  
| ---------               | -------- | -------                                                          |
| awsenv_download_url     | yes      | https://github.com/mauromedda/awsenv/releases/download           |
| awsenv_release_version  | yes      | 0.11.3                                                           |    
| awsenv_release_platform | yes      | "{{ ansible_system\|lower }}"                                     |     
| awsenv_release_cpuset   | yes      | amd64                                                            |
| awsenv_artifact         | yes      | "awsenv_{{ awsenv_release_platform }}_{{awsenv_release_cpuset}}" |


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible_role_awsenv, awsenv_release_version: 0.11.3,  awsenv_release_cpuset: amd64}

License
-------

BSD

Author Information
------------------

misurellig < bejohnzorn at gmail dot com >
