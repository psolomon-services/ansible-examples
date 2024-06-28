# Ansible Project

The following playbooks (and roles) were copied from my private ansible repo.
All private information (config) has been removed.

Playbooks:
- `awx.yml`:                     _full deploy of an AWX setup, including UI setup (project/inventory/templates/etc.)_
  - this was written prior to moving to kubernetes (but the k8s deploy still needs ansible UI setup from this playbook)
  - the goal for this project was for an out of the box installtion (i.e. log in, press a button, deploy pihole, with no additional changes to the AWX UI)
- `info.yml`:                    _similar to ping, gives more info on nodes_
- `jenkins.yml`:                 _jenkins install, from CASC (the CASK setup is in Ansible vault because of some private certs, but has been removed from this repo)_
- `pihole-test-dns-lookups.yml`: _test pihole DNS setup_
- `pihole-update-adlists.yml`:   _update adlists (with option to turn each ON or OFF)_
- `pihole-update-dns.yml`:       _updates pihole local DNS list_
- `pihole.yml`:                  _full pihole install, including adlists and local DNS_
- `ping.yml`:                    _normal Ansible ping playbook_
- `test-collections.yml`:        _tests loading of collections_
- `test-vault-secrets.yml`:      _tests retrieval of secrets (Ansible Vault) and non-secrets_

Other:

- `inventory`:                   _local, non-dynamic Ansible inventory (for my home lab)_
- `host_vars`:                   _host-related config_
- `group_vars`:                  _group-related config and a vault file_
- `roles`:                       _roles for above playbooks_
