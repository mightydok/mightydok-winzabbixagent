Role Name
=========

Simple and dirty role to install zabbix agent 3 on windows server

Requirements
------------

None

Role Variables
--------------
```
winzabbixagent_zabbix_server: 127.0.0.1
winzabbixagent_listenport: 10050
winzabbixagent_listen_ip: 0.0.0.0
winzabbixagent_zabbix_server_active: 127.0.0.1
```
Dependencies
------------

None

Example Playbook
----------------

Simple role:
```
---
# Playbook for zabbix agent install
-   name: Install zabbix on all servers
    hosts: all
    roles:
    - mightydok.winzabbixagent
```

License
-------

BSD

Author Information
------------------

Name: Vitaliy Okulov   
Email: vitaliy.okulov@gmail.com
