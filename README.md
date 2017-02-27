Role Name
=========

Name: ***mightydok.winzabbixagent***   
Simple and dirty role to install zabbix agent 3 on windows server   

* files/externalscripts - folder for custom monitoring script   
* files/userparameters - folder for custom conf files to include in zabbix agent configuration   

Role logic:
* Copy msi file from file/msi to c:\windows\temp
* Place config file from template
* Remove C:\zabbixdata folder
* Copy files/externalscripts and files/userparameters to C:\zabbixdata
* Restart zabbix agent
* Ensure zabbix agent started and make autostart mode on

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
