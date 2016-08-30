Role Name
=========

This role is to install and provide basic configuration of Red Hat Satellite 6.2+ on a RHEL 7+ machine. 

Requirements
------------
1) Ansible must be installed. (Version 2.1+ recommended).

2) RHEL 7+ and RH Satellite 6.2+ with valid subscriptions.
You must first provide a Satellite Manifest file
for the playbook to work properly. Follow the below steps.

3) A valid Satellite manifest

- Navigate and login to the [Red Hat Network](https://rhn.redhat.com)
- Select "Subscriptions"
- Select "Satellite" under "Subscription Management Applications"
- Select "Register a Satellite"
- Enter a name, the version of Satellite, and click Register
- Select "Attach Subscription" and choose which subscription to attach
- Select "Download Manifest" 
- Place the zipped file under /files in the ansible6-installer role directory

Variables
--------------
All variables can be found under vars/main.yml

Dependencies
------------
No dependencies for this role. 

Running the playbook
----------------
If running satellite.yml directly from the role directory, make update hosts.target with the address corresponding to your target server.

If intended for use with other roles, include the role in a playbook located at your top level Ansible directory.

Example: [ansible_directory]/playbook.yml
- name: This is an example playbook
  hosts: desired_hostname
  roles:
    - include: satellit6-install

License
-------

BSD

Author Information
------------------

Josh Springer <springer@redhat.com> 
[GitHub](https://github.com/jdspringr07)
