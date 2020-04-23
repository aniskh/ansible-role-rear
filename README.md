Role Name
=========

An Ansible role to install and configure Relax and Recover (ReaR) tool

Requirements
------------
None.

Role Variables
--------------
Available variables are listed below, along with default values (see `defaults/main.yml`):

 rear_output: 'ISO'
 rear_type: 'NETFS'
 rear_cron_user: root
 rear_cron_day: '*'
 rear_bkp_url
 rear_cron_min
 rear_cron_hour

If "rear_cron_min" and "rear_cron_hour" are not specified, the cron configuration will be omitted.
By default, the crontab created run the ReaR in backup mode ("mkbackup").

Dependencies
------------
None.

Example Playbook
----------------
 - hosts: all
   roles:
     - role: rear
       rear_bkp_url: "nfs://192.168.122.111/backup"
       rear_cron_min: '0'
       rear_cron_hour: '2'
 

License
-------

GPL

Author Information
------------------
This role was created in 2020 by Anis KHACHNAOUI [ systems /devops Engineer ]
