```yml
---
- hosts: all
  tasks:
  - name: Update Server
    yum:
      name: '*'
      state: latest
    register: task_result

  - name: reboot server if there was an update
    reboot:
      reboot_timeout: 60
    when: task_result is changed

  - name: ping host
    ansible.builtin.ping:
```
