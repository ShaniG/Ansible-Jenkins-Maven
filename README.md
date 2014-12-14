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

    --- 
    hostname: localhost  
    jenkins_jar_location: /opt/jenkins-cli.jar #Location you store the jenkins jar
    jenkins_plugins: # Jenkins plugins found on: https://wiki.jenkins-ci.org/display/JENKINS/Plugins
        - git
        - sonar
        - ssh
    jenkins_maven_job_name: mavengit #name of the jenkinsjob
    jenkins_git_url: https://github.com/ShaniG/integrationtest.git #github url
    #jenkins_git_url: git@github.com:ShaniG/integrationtest.git # SSH git URL
    #jenkins_ssh_key: public sshkey (common: id_rsa.pub ) 
    #jenkins_private_ssh_key: private sshkey (common: id_rsa ) 

Dependencies
------------

No dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: CIServer
      roles:
         - jenkins

License
-------

BSD, MIT

Author Information
------------------

- ShaniG (Based on: https://github.com/geerlingguy/ansible-role-jenkins)
 
