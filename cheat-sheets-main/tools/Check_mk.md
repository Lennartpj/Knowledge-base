Checkmk is software developed in Python and C++ for IT Infrastructure monitoring. It is used for the monitoring of servers, applications, networks, cloud infrastructures, containers, storage, databases and environment sensors.



### Troubleshoot
---
#### Linux:
##### Check_mk Version
```Bash
cmk-agent-ctl --version
```
##### Check_mk Status
```Bash
cmk-agent-ctl status
```

##### Check_mk agent register
```bash
cmk-update-agent register -s checkmk -i monitoring -H $HOSTNAME -p http -U cmkadmin -P ******* -v
```

 firewall-cmd --add-port=6556/tcp --permanent
 firewall-cmd --reload