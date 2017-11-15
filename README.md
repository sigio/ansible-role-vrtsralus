Role Name
=========

This role installs the VRTS-ralus agent for BackupExec on RHEL 7.x / CentOS 7.x. Since the package isn't very compatible with EL7, all its brokenness is fixed by this role.

Requirements
------------

The required rpm's for VRTS-ralus should be placed in the files/ subdirectory, see the Readme file in that directory.

Role Variables
--------------

Create a list of ip-addresses named 'backup_servers' to which the firewall will be opened. Example:

backup_servers:
  - 10.0.0.100
  - 10.0.0.101
  - 10.0.0.102

If using a firewall (firewalld), create a variable
  - firewalld_enabled: true

Specify an encrypted password for the svc_beuser account in 'vrtsralus_password'

Other variables are documented in the defaults/main.yml file

Dependencies
------------

None, besides an EL7 distro

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: sigio.vrtsralus }

License
-------

BSD

Author Information
------------------

Mark Janssen <mark@sig-io.nl>
Sig-I/O Automatisering
