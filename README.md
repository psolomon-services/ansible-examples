# Ansible Projects

The following playbooks (and roles) were copied from my private Ansible repo, which include several of my home lab projects.  All private information (config) has been removed.

*NOTE:  These playbooks and roles were written mostly from scratch, to facilitate Ansible learning!*

## TODOs

_Most of my TODOs are related to splitting up roles and cleaning up the playbooks_

## Playbooks

- `awx.yml`:                     _full deploy of an AWX setup, including UI setup (project/inventory/templates/etc)_
  - _This was written prior to moving to Kubernetes (but for now, the K8s deploy still needs Ansible UI setup from this playbook, due to lack of K8s CRDs for resources like `Projects` and `Inventory`)_
  - _The goal for this project was for an out of the box installation (i.e. log in, press a button, deploy pihole, with no additional changes to the AWX UI)_
  - _NOTE:  this AWX playbook installs all playbooks, below, plus others, not covered here_
- `info.yml`:                    _similar to ping, gives more info on nodes_
- `jenkins.yml`:                 _jenkins install, from CASC plugin (the CASC setup is in Ansible vault because of some private certs, but has been removed prior to creating this repo)_
  - _similar goal to AWX, out of box full setup -- *IN PROGRESS*_
- `pihole.yml`:                  _full pihole install, including docker setup, nginx reverse proxy, unbound, adlists, and local DNS config_
- `pihole-test-dns-lookups.yml`: _test pihole DNS setup_
- `pihole-update-adlists.yml`:   _update adlists (with option to turn each ON or OFF, messy, but it works for now)_
- `pihole-update-dns.yml`:       _updates pihole local DNS list_
- `ping.yml`:                    _normal Ansible ping playbook_
- `test-collections.yml`:        _tests loading of collections_
- `test-vault-secrets.yml`:      _tests retrieval of secrets (Ansible Vault) and non-secrets_

## Inventory
- `playbooks/inventory`:         _local, non-dynamic Ansible inventory (for my home lab)_

## Config and Other

- `playbooks/host_vars`:         _host-related config_
- `playbooks/group_vars`:        _group-related config and a vault file_
- `roles`:                       _roles for above playbooks_
