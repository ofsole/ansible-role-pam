Ansible-role-pam
=========

[![Build Status](https://travis-ci.org/ofsole/ansible-role-pam.png?branch=master)](https://travis-ci.org/ofsole/ansible-role-pam)

This role manages pam on RedHat, Suse and Ubuntu

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.
```
# defaults file for ansible-role-pam
config_file: '/etc/security/limits.conf'
config_file_mode: 640
limits_d_dir: '/etc/security/limits.d'
limits_d_dir_mode: 750
config_file_lines: []
allowed_users: 'root'
login_pam_access: 'required'
sshd_pam_access: 'required'
ensure_vas: 'absent'
pam_conf_file: '/etc/pam.conf'
pam_d_login_path: '/etc/pam.d/login'
pam_d_login_owner: 'root'
pam_d_login_group: 'root'
pam_d_login_mode: 644
pam_d_sshd_path: '/etc/pam.d/sshd'
pam_d_sshd_owner: 'root'
pam_d_sshd_group: 'root'
pam_d_sshd_mode: 644
pam_d_other_file: '/etc/pam.d/other'
common_auth_file: '/etc/pam.d/common-auth'
common_auth_pc_file: '/etc/pam.d/common-auth-pc'
common_account_file: '/etc/pam.d/common-account'
common_account_pc_file: '/etc/pam.d/common-account-pc'
common_password_file: '/etc/pam.d/common-password'
common_password_pc_file: '/etc/pam.d/common-password-pc'
common_session_file: '/etc/pam.d/common-session'
common_session_pc_file: '/etc/pam.d/common-session-pc'
common_session_noninteractive_file: '/etc/pam.d/common-session-noninteractive'
system_auth_file: '/etc/pam.d/system-auth'
system_auth_ac_file: '/etc/pam.d/system-auth-ac'
vas_major_version: '4'
allowed_users: 'root'
pam_d_login_oracle_options: 'UNSET'
_services: {}
limits_fragments: ""
#for accesslogin.yml file
access_conf_path: '/etc/security/access.conf'
access_conf_owner: 'root'
access_conf_group: 'root'
access_conf_mode: '644'
access_conf_template: 'access.conf.j2'
```

Dependencies
------------

ansible-role-nsswitch

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-pam, ensure_vas: present }

License
-------

BSD

Author Information
------------------

Elvis Cai
