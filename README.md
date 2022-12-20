# ansible-update-hosts
Ansible role to update computing nodes list in a HTCondor managed cluster

## pdsh was depricated in RHEL 9
For that reason we are migrating to [pssh](https://linux.die.net/man/1/pssh), which is a very similar tool, but uses dedicated host files for each group instead of a single gender file with all the groups.
If you still want to use `pdsh`, make sure to set `update_hosts_genderfile` to true, in order to keep your genderfile updated.