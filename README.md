# cfme upgrade ansible

On this project i will developing automation based on ansible to ugrade CFME appliances.

## User manual:

### pre-condition
Before using this playbook, make sure ssh to any host is allowed with root user and without password.

### upgrade role installation
After you verified that ansible installed on your system you have to install the upgrade role
before you can use it

I recommend on installation directly from GitHub, that insure you will get code's latest version
the command for remote installation is:
```ansible-galaxy install git+https://github.com/shalomnaim1/cfme_upgrade_ansible.git,master```

### Ansible playbook run command
ansible-playbook -i inventory.file cfme_upgrade_playbook.yaml

## Input files structure:
### Inventory file:
The inventory file contain some variables in addition to the ip address/hostnames of remote systems to be updated

**variables description**
repos - yum repositories which contain the target CFME version
username - username for subscription manager
password - password for subscription manager

**inventory example:**

[cfme-appliances:vars]
repos=["repo1","repo2","repo3"]
password=123456
username=root

[cfme-appliances]
10.35.70.96


