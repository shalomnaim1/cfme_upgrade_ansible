# cfme upgrade ansible

on this project i will developing automation based on ansible to ugrade CFME appliances.

the automation will use inventory file that include all the target system to upgrade and
repo list file which contain urls of repositories with the latest version of CFME.

## User manual:

before using this playbook, make sure ssh to any host is allowed with root user and without password.

**Ansible playbool run command:**
ansible-playbook -i hosts cfme_upgrade_playbook.yaml

## Input files structure:
### Inventory file:

**example:**

[cfme-appliances:vars]
repos=["repo1","repo2","repo3"]
password=123456
username=root

[cfme-appliances]
10.35.70.96


