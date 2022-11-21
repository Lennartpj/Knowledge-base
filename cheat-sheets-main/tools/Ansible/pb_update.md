```yml
---
- name: Update and restart Server
  hosts: all
  tasks:
  - name: Update Server
    yum:
      name: '*'
      state: latest
    register: task_result

  - name: reboot server if there was an update
    reboot:
    when: task_result is changed

  - name: Update Server second try
    yum:
      name: '*'
      state: latest
```
