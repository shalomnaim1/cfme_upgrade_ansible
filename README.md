# cfme_upgrade_ansible

on this project i will developing automation based on ansible to ugrade CFME appliances.

the automation will use inventory file that include all the target system to upgrade and
repo list file which contain urls of repositories with the latest version of CFME.

## User manual:

before using this playbook, make sure ssh to any host is allowed with root user and without password.

**Ansible playbool run command:**
ansible-playbook cfme_upgrade_playbook.yaml -i hosts -u root -e
{"username":"username","password":"password","repos":["http://url/to/repo/1","http://url/to/repo/2..."]}

## Input files structure:
### Inventory file:
The inventory file contain only one group named cfme-appliances

**example:**

[cfme-appliances]
10.35.70.96
