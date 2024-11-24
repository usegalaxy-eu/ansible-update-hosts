# ansible-update-hosts

Ansible role to update computing nodes list in an HTCondor-managed cluster

## pdsh was deprecated in RHEL 9

For that reason, we are migrating to [pssh](https://linux.die.net/man/1/pssh), a very similar tool that uses dedicated host files for each group instead of a single gender file with all the groups.
If you still want to use `pdsh`, make sure to set `update_hosts_genderfile` to true, to keep your genderfile updated.
