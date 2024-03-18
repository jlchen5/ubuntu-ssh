# SSH Configuration Guide for Ubuntu
## Introduction
This README provides a detailed guide on how to configure SSH (Secure Shell) on an Ubuntu system. SSH is a protocol allowing secure remote login from one computer to another.

Prerequisites
An Ubuntu server
A non-root user with sudo privileges

- Step 1: Install SSH
```bash
sudo apt update
sudo apt install openssh-server
```

Check the status of the SSH service:
```bash
sudo systemctl status ssh
```
- Step 2: Configure SSH (Optional)
Edit the SSH configuration file:
```bash
sudo nano /etc/ssh/sshd_config
```

Make necessary changes, like changing the default port or disabling root log in.

Restart SSH service to apply changes:

```bash
sudo systemctl restart ssh
```
- Step 3: Connect from Client
From the client machine, connect to the server:

```bash
ssh your_username@server_ip_address
```
Replace your_username and server_ip_address with your actual username and server IP.

- Step 4: Additional Security (Optional)
Set up SSH keys for a passwordless login.
Configure firewalls and fail2ban to enhance security.
```bash
sudo ufw allow ssh
```

## Conclusion
This guide covers the basics of setting up SSH on Ubuntu. Adjust settings according to your security needs and environment.
