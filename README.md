#  UFW Firewall Rule Testing

##  Description
This project demonstrates how to configure and manage firewall rules using **UFW (Uncomplicated Firewall)** on a Linux-based system. It includes practical steps to block and allow traffic on specific ports, test the effectiveness of the rules, and understand how firewalls help protect systems by filtering network traffic.

##  Tools Used
- **Kali Linux** (or any Debian-based Linux)
- **UFW** (Uncomplicated Firewall)
- **Telnet** (for testing blocked ports)
- **Terminal**

##  Task Objectives
1. View existing firewall rules
2. Block inbound traffic on port 23 (Telnet)
3. Test if the rule works
4. Allow traffic on port 22 (SSH)
5. Delete the Telnet rule
6. Summarize how firewalls filter traffic

##  Commands Used
# View current UFW rules
sudo ufw status numbered

# Deny Telnet (Port 23)
sudo ufw deny 23/tcp

# Test the block using Telnet
telnet localhost 23

# Allow SSH (Port 22)
sudo ufw allow 22/tcp

# Remove the Telnet block rule
sudo ufw delete deny 23/tcp
