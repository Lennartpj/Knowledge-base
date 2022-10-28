


```yml
--- 
- hosts: yum 
  tasks:
  - name: Update all installed packages using YUM module 
    yum: 
      name: '*' 
      state: latest 
      update_cache: yes 
      update_only: yes
      register: yum_update_status
      
  - name: Reboot when packages were updated 
    reboot: 
    when: yum_update_status.changed
```