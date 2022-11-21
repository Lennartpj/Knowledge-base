
```yml
---
- name: install and register the check_mk agent
  hosts: all
  tasks:
  - name: set firewall
	firewalld:
      port: 6556/tcp
      permanent: yes
      state: enabled
      immediate: yes
      
  - name: install check_mk agent
    yum:
      name: check-mk-agent
      state: latest
	register: task_result

  - name: register check_mk agent
    
```