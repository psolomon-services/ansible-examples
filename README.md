# Ansible Project

The following playbooks (and roles) were copied from my private ansible repo.  All private information has been removed.

Playbooks:
- awx.yml:                     full deploy of an AWX setup, including UI setup (project/inventory/templates/etc.)
  - this was written prior to moving to kubernetes (but the k8s deploy still needs ansible UI setup from this playbook)
  - the goal for this project was for an out of the box installtion (i.e. log in, press a button, deploy pihole, with no additional changes to the AWX UI)
- info.yml                     similar to ping, gives more info on nodes
- jenkins.yml                  jenkins install, from CASC (the CASK setup is in Ansible vault because of some private certs, but has been removed from this repo)
- pihole-test-dns-lookups.yml  test pihole DNS setup
- pihole-update-adlists.yml    update adlists (with option to turn each ON or OFF)
- pihole-update-dns.yml        updates pihole local DNS list
- pihole.yml                   full pihole install, including adlists and local DNS
- ping.yml:                    normal Ansible ping playbook
- test-collections.yml:        tests loading of collections
- test-vault-secrets.yml:      tests retrieval of secrets (Ansible Vault) and non-secrets

Other:

- inventory                    local, non-dynamic Ansible inventory (for my home lab)
- host_vars                    host-related config
- group_vars                   group-related config and a vault file
- roles                        roles for above playbooks
