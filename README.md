## Ansible cli playbook on hosts

In the ansible.cfg we have edited the inventory line to use the hosts fil in this repo directory, so we run all ansible commands within this repo.

``
inventory      = hosts
-- Default settings
inventory      = /etc/ansible/hosts
``

In our hosts file we specify the target host we wanna run Ansbile on, in this case we have a server up on the ip adress 192.168.1.250 and we will run the playbook as the user ansible on that host.

``
192.168.1.250 ansible_user=ansible
``

Im using Oracle Virtual Box with a CentOS cli version for this demo.

### Playbook example with roles only
Copy over app and yum installations 

``
playbook-roles.yml
``

### Playbook example with tasks only
Copy over app and yum installations 

``
playbook-taks.yml
``

### Playbook example combines with roles and tasks
Copy over app, yum installations, installing consul and running consul on host

``
playbook.yml
``