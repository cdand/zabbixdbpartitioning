zabbixdbpartitioning
====================

Modified script to automate the creation of Zabbix MySQL DB partitions with Zabbix 2.0.x

This work is heavily copied from work by jbayer published on linuxnotes.us (http://linuxnotes.us/archives/503).

In turn that article is derived from work by Ricardo Santos published on the zabbixzone.com blog (http://zabbixzone.com/zabbix/partitioning-tables/).

My efforts extend the contributions of the above authors to make the database partitioning compatible with Zabbix 2.0.x which uses foreign keys between certain histortical tables, my solution to this has been to only partition the history and trends tables. This does leave a problem of a solution to perform some kind of 'housekeeping' on tables such as events, alarms and acknowledes etc...

I have also added a few more arguments to the script that allow a non-interactive functionality (e.g. for use with Puppet) and with this modified/added some default values.
