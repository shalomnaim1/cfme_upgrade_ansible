# cfme_upgrade_ansible

on this project i will developing automation based on ansible to ugrade CFME appliances.

the automation will use inventory file that include all the target system to upgrade and
repo list file which contain urls of repositories with the latest version of CFME.

## User manual:

borofe using this playbook, make sure ssh to any host is allowed with root user and without password.

**Ansible playbool run command:**
ansible-playbook cfme_upgrade_playbook.yaml -i hosts -u root
    -e "username=user_for_subscriber_manager password=password_for_subscriber_manager"



## Input files structure:
### Inventory file:
The inventory file contain only one group named cfme-appliances

**example:**

[cfme-appliances]
10.35.70.96

### Repo list file:
This is file on yum db format, each repo contain 4 args:
1) repo name
2) repo url
3) repo state enbaled
4) gpg disable flag

**example:**

[update-0]
name=update-url-0
baseurl=http://url/to/repo
enabled=1

gpgcheck=0
