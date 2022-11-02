
### Generate [[ssh]] key pair

```bash
[user@host ~]$ ssh-keygen
Generating public/private rsa key pair. 
Enter file in which to save the key (/home/user/.ssh/id_rsa): Enter
Created directory '/home/user/.ssh'. 
Enter passphrase (empty for no passphrase): Enter 
Enter same passphrase again: Enter
Your identification has been saved in /home/user/.ssh/id_rsa.
Your public key has been saved in /home/user/.ssh/id_rsa.pub. 
The key fingerprint is:
SHA256:veutUNPio3QDCyvkYm1oIx35hmMrHpPKWFdIYu3HV+w user@host.lab.example.com
The key's randomart image is: 
+---[RSA 2048]----+ 
|                 | 
|   .     .       | 
|  o o     o      | 
| . = o   o .     | 
|  o + = S E .    | 
| ..O o + * +     | 
|.+% O . + B .    | 
|=*oO . . + *     | 
|++.     . +.     | 
+----[SHA256]-----+ 
```

By default, your private and public keys are saved in your `~/.ssh/id_rsa` and `~/.ssh/id_rsa.pub` files, respectively.

### Share public ssh key

For all of this to work, you need to share your public key with the remote machines you are trying to SSH to. Use the `ssh-copy-id` command to copy your public key over to the destination system. By default, the file path is `/home/user/.ssh/id_rsa.pub`. You issue the command, specify the file you are sharing, then the user/host we are sharing it with. It should look like this:

```bash
ssh-copy-id user@destination
```

If you have saved the public ssh key in a different directory use the parameter -i and specify the path. for example:

```bash
ssh-copy-id -i ~/.ssh/id_rsa.pub user@destination
```

### Advantages and summary

The advantages of using [[SSH]] key-based authentication are clear. Passwords are stolen every day, mainly due to human error but also due to attacker skill and determination. An encrypted key, and more specifically, a password-protected encrypted key, makes your SSH authentication even more difficult to attack. You still need to strike a balance of availability and security, but that is handled differently in every environment.