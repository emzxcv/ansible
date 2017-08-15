# Ansible configuration scripts for couchdb and twitter harvesters

### Requires ansible 2.3 or newer


## Configuration
take the hosts file generated from the boto instance setup, or manually fill in values in supplied file

#### Note: Couchdb and twitter harvesters should be on different instances, harvesters can be on the same instance however this is more likely to result in throttling occuring on the twitter api and is not recommended

##Run

### Install Docker only
ansible-playbook -i hosts install-docker.yml -c paramiko

### Install/Start couchdb
ansible-playbook -i hosts couchdb.yml -c paramiko

### Install/Start searchers
ansible-playbook -i hosts searcher.yml -c paramiko

### Install/Start backfill
ansible-playbook -i hosts backfill.yml -c paramiko

