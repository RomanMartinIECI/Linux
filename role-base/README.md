Role Base
=========

This role configures basic setting in SO, like base and update repositories, time zone, ntp servers, dns servers...

Requirements
------------

A Red Hat Linux, CentOS or Oracle Linux system.

Role Variables
--------------

- base_config_repos: If repositories should be configured for the OS (e.g. yes)
- base_repos: List of repositories to configure
    - name: Name for the repo (e.g. 'centos-7-base')
    - description: Description for the repo (e.g. 'CentOS 7.2 base (x86_64)')
    - baseurl: URL for access to repo (e.g. 'http://mirror.centos.org/centos/el7/updates/x86_64/')
    - file: Name of the .repo file (e.g. 'centos-7')
    - enabled: If the repo is enabled or not (e.g. 'yes')
    - distribution: Name of Linux distribution. 'CentOS', 'OracleLinux' or 'RedHat' (e.g. 'CentOS')
    - version: Major version 
    - release: Release of OS version 

- base_timezone: Time zone for OS (e.g. 'Europe/Madrid')
- base_hostname: Set specified hostanme (e.g. 'server1')
- base_root_password: Define root password (e.g. 'Pasword123')
- base_dns_servers: List of DNS servers in order of preference (e.g. '8.8.8.8')
- base_dns_search: List of search domains (e.g. 'domain1.org domain2.net')
- base_dns_domain: Domain name for DNS (e.g. 'domain.com')
- base_ntp_servers: List of NTP servers (e.g. 'hora.roa.es')
- base_swap_size: New size of the swap memory (e.g. 16384)
- base_swap_mem: Threshold of memory to resize swap. If memory is greater than this value then swap is resized to base_swap_size (e.g. 8192)
- base_extra_packages: List of packages to install from repository

Example Playbook
----------------
All these variables are optional and only are set if defined, except repositories that are configured by default.
```
base_config_repos: yes

base_timezone: 
base_hostname: 
base_root_password: 

base_dns_servers:
   - 
   
base_dns_domain: 

base_ntp_servers:
   - 

base_swap_size:
base_swap_mem: 

base_extra_packages:
   - sysstat
   - telnet
   - net-tools
```
Author Information
------------------

IT_AUTOMATION
