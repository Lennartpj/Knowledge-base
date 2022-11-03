# User Management

COMMAND | DESCRIPTION
---|---
`sudo adduser username` | Create a new user
`sudo userdel username` | Delete a user
`sudo usermod -aG groupname username` | Add a user to group
`sudo deluser username groupname` | Remove a user from a group
`passwd username` | change Password
`sudo -l -U user_name` | see if user has sudo rights
`sudo visudo` | change sudoer file



# Permit AD Users and Groups

###  Add AD Groups
```bash
sudo realm permit -g group@domain.de
```

### Give root permission to group
```Bash
echo '%group@domain.de ALL=(ALL:ALL) ALL' | sudo EDITOR='tee -a' visudo
```

### AD User
```Bash
sudo realm permit -g account@domain.de
```

### Give root permission to user
```Bash
sudo usermod -aG wheel account@domain.de
```
