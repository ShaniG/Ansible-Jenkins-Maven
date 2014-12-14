Jenkins-Maven
=========

This is an ansible role to create a CI server Jenkins. This role includes automatic job creation for Maven linked to your own Github repository (https). There is also a commented section for SSH connection with your Github Repository.

SSH requires an additional setting on your job configuration (jenkins dashboard):
* Go to configuration of the job.
* Click 'Add' credentials below Github url.
* Choose for Kind: SSH Username with private key
* Under private key select: "From the Jenkins master ~/.ssh"
* Click on 'Add'
* Select 'jenkins' as credentials and now SSH works !
    

Requirements
------------

No requirements.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

No dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD, MIT

Author Information
------------------

- ShaniG (Based on: https://github.com/geerlingguy/ansible-role-jenkins)
 
