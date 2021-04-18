# Ansible Role: aws_ec2_dynamic_inventory
=========

A simple Ansible role for getting the AWS ec2 instances IP's dynamically using tags.


It will install the following:-
------------
  
  ansible
  boto
  boto3
  
Role Name
=========

A brief description of the role goes here.
This role is used for them having the AWS account wether it is the free-tier account or the educate account and get the ec2 instance's ips having in that AWS account.

Requirements
------------

Pre-requisite for using this role is you must have yum configured if you are using Rhel OS or if any other OS installing tool should be available.

Attention
---------

As when we create any insytance we give tags. So both the python script will Create inventory groups using tags modify as you use them in your environment.

For getting the group of tags so to your /etc/ansible/host directory use this command:- "python3 ec2.py" 
Now you can see all your instance ip's with their following tags.

You can also use these tags.
In my case I used it as follows in ec2_instances_facts.yml.

    hosts: tag_Name_Production
     
    hosts: key_mykey
     
Role Variables
--------------

A description for role variables goes here.

| Variable                                     | File                          | Comments                                     
| :---                                         | :---                          | :---       
|                                              |                               |
| `aws_region:`                                | vars/main.yml                 | Inform AWS Region
|                                              |                               |
| `aws_access_key`                             | vars/credentials.yml          | Inform AWS Access Key
|                                              |                               |
| `aws_secret_key`                             | vars/credentials.yml          | Inform AWS Secret Key
|                                              |                               |
| `aws_security_token`                         | vars/credentials.yml          | Inform AWS Security Token(if having)
|                                              |                               |
| `path_to_your_inventory_dir`                 | vars/main.yml                 | Inform inventory directory name
|                                              |                               |
| `path_to_your_ansible_cfg_file`              | vars/main.yml                 | Inform of the ansible config file
|                                              |                               |

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- hosts: localhost
  
  gather_facts: no

  roles:

    - /path/aws_ec2_dynamic_inventory

...
License
-------

BSD

Official documentation of the modules of this role
--------------------------------------------------

https://docs.ansible.com/ansible/latest/modules/ec2_instance_info_module.html
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/lineinfile_module.html
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/replace_module.html
https://docs.ansible.com/ansible/latest/modules/template_module.html


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://www.linkedin.com/in/komal-suthar-3383a61b5

![](https://visitor-badge.glitch.me/badge?page_id=24-komal.aws_ec2_dynamic_inventory)


