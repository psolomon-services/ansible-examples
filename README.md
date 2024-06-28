# Ansible Project

The following playbooks (and roles) were copied from my private ansible repo.
All private information (config) has been removed.

*NOTE:  These playbooks and roles were, for the most part, written from scratch, to facilitate Ansible learning.*

## TODOs

_Most of my TODOs are related to splitting up roles and cleaning up the playbooks_

## Playbooks

- `awx.yml`:                     _full deploy of an AWX setup, including UI setup (project/inventory/templates/etc.)_
  - _this was written prior to moving to kubernetes (but the k8s deploy still needs ansible UI setup from this playbook, due to lack of CRDs for things like `Projects` and `Inventory`)_
  - _the goal for this project was for an out of the box installation (i.e. log in, press a button, deploy pihole, with no additional changes to the AWX UI)_
  - _this is definitely my most complex playbook/role_
  - _NOTE:  this awx playbook installs most, if not all, of the following playbooks (as Templates) in the AWX UI_
- `info.yml`:                    _similar to ping, gives more info on nodes_
- `jenkins.yml`:                 _jenkins install, from CASC plugin (the CASC setup is in Ansible vault because of some private certs, but has been removed from this repo)_
  - _similar goal to AWX, out of box full setup_
- `pihole.yml`:                  _full pihole install, including docker setup, nginx reverse proxy, unbound, adlists, and local DNS config_
- `pihole-test-dns-lookups.yml`: _test pihole DNS setup_
- `pihole-update-adlists.yml`:   _update adlists (with option to turn each ON or OFF)_
- `pihole-update-dns.yml`:       _updates pihole local DNS list_
- `ping.yml`:                    _normal Ansible ping playbook_
- `test-collections.yml`:        _tests loading of collections_
- `test-vault-secrets.yml`:      _tests retrieval of secrets (Ansible Vault) and non-secrets_

## Other

- `inventory`:                   _local, non-dynamic Ansible inventory (for my home lab)_
- `playbooks/host_vars`:         _host-related config_
- `playbooks/group_vars`:        _group-related config and a vault file_
- `roles`:                       _roles for above playbooks_
