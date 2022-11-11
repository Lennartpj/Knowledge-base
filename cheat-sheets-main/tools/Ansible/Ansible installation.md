
If you want to know what Ansible is have a look here: ([[Ansible]])

This Page deals with how to Install **Ansible**. On a Redhat RHEL 8 Server.


First check if Ansible is already installed with the command:

```Bash
ansible --version
```

If Ansible is not installed follow these Steps

### **Step 1: Update RHEL 8**

To install Ansible, first log in to your system and update the system packages using the command:

```Bash
sudo dnf update -y
```

### **Step 2: Install Python3 on RHEL 8**

By default, RHEL 8 comes with Python3 installed. To check this use the command:

```Bash
python3 -V
```

If by any chance Python 3 is missing from your system, simply run the command:

```Bash
sudo dnf install python3
```

### **Step 3: Install Ansible**

With the prerequisites in check, now proceed and install Ansible using the commands:

```Bash
sudo  dnf -y install ansible
```

### Problem with dnf
if the command dnf is not recognised:
```Bash
sudo yum install dnf
```