# **Troubleshooting Cookbook**
Random collection of stuff I can't remember, thoughts and findings throughout my various troubleshooting voyages.

# **Systemd

# **Firewalls**

## **ufw**
Uncomplicated firewall, acts as a wrapper for iptables and is usually installed by default on Ubuntu distributions.

### **commands**
- `sudo ufw enable` - turns ufw on
- `sudo ufw status verbose`
- `sudo ufw status numbered` - show order of rules
- `sudo ufw allow <service name>`
- `sudo ufw allow from <ip> to port <port>`
- `sudo ufw allow from <ip> to port <port> proto <protocol>`
- `sudo ufw deny from <ip or subnet> to any port <port>`
- `sudo ufw delete <rule number>`
- `sudo ufw insert <rule number> allow from <ip>`

## **iptables**
One of the OGs for OS level firewall rules on Linux systems. 


## **firewalld**

###



