# TODO

* AWX workflow:  can you label jobs that are the same job but with different args?
* pihole dns:  add fixed IP containers (unbound, etc.)
* staging control node?
* look into ansible tests
  * built-in
  * molecule? (might still be in closed beta)
* ansible-galaxy
  * "For anyone else who reads this - this is how I fixed it: Copy the default "Ansible Galaxy" credential that you cannot edit from the UI. Go to galaxy.ansible.com, login/link GH account, and then get your API token from your preferences in the top right. Copy that, edit the copied credential in AWX, add the API token you copied, assign your org to the token, then go to organizations and change the credentials to that of your copy. This worked for me"
* import\_task vs. include\_task vs. include
* build container images?
