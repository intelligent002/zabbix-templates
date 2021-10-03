# D-Link DGS 1100-16 firmware 1.01.B053
### Zabbix template is for public usage

The device is pretty simple, therefore modular templates shipped with the Zabbix instance can handle the most of load.

Please import templates in the following order:

1. *Template Module EtherLike-MIB SNMP* - **if not present**, a common template that perform duplex mode discovery.
2. *Template Module Generic SNMP* - **if not present**, a common template that performs ICMP ping of target device and keep some related metrics.
3. *Template Module Interfaces Simple SNMP* - **if not present**, a common template that works with 32bit interface counters via SNMP.
4. *Template Module Interfaces SNMP* - **if not present**, a common template that works with 64bit interface counters via SNMP, **it is strictly optional, and is not used by main template** supplied just as a pair for its 32bit brother.
5. **D-Link DGS 1100-16** - finally.

> Importing templates in different order will fail the operation as main template relies on the common ones.