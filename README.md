eucalyptus-nc
=========

Installs and configure eucalyptus-nc

Requirements
------------

CentOS 6.6

Role Variables
--------------

NC Specific

| Parameter | Required | Default | Description
|--- |--- |--- |---
| bridge_number | Yes | 0 | ID for the bridge
| cpu_overcommit | No | 1 | Value for the overcommit (1 = no overcommit)
| managed_addrpernet | Yes | 32 | Multiple of 8 > 32
| instance_dns_domain | Yes | eucalyptus.internal | Name for the DHCP search config (for Managed modes)
| iface_name | Yes | None | The interface on which the bridge is
| networking_mode | Yes | EDGE | Networking mode (EDGE recommended)
| edge_using_private | No | True | Meta-Data using private addresses
| partition | Yes | None | Name of the Availability Zone (cluster)
| vnet_netmask | No | None | Network for instances (for MANAGED modes)
| vnet_subnet | No | None | Subnet for instances (for MANAGED modes)
| instance_dns_server | No | None | IP of the DNS server (for MANAGED modes)


= Eucalyptus Generic =

| Parameter | Required | Default | Description
|--- |--- |--- |---
| euca_repo_url | Yes | Latest RPM URL | URL to the wanted eucalyptus rpm
| euca2ools_repo_url | Yes | Latest RPM URL | URL to the wanted euca2ools rpm
| epel_repo_url | Yes | Latest RPM URL | URL to the latest EPEL rpm
| elrepo_repo_url | Yes | Latest RPM URL | URL tp the latest elRepo rpm
| euca_local_repo_url | No | None | URL to a local Eucalyptus Repo
| euca_repo_file | Yes | /etc/yum.repos.d/eucalyptus.repo | Path to the repo file
| euca2ools_local_repo_url | No | None | URL to a local euca2ools repo
| euca2ools_repo_file | Yes | /etc/yum.repos.d/euca2ools.repo | Path to the repo file
| euca_use_local_repo| No | False | Use local repos URL or not
| euca_images | Yes | eucalyptus-service-image | List of the eucalyptus images packages
| euca_conf_file_path | Yes | /etc/eucalyptus/eucalyptus.conf | Path to the root eucalyptus.conf file

Dependencies
------------

JohnPreston.BridgeCreator

Example Playbook
----------------


License
-------

GPLv3

Author Information
------------------

John Preston [John Mille]

