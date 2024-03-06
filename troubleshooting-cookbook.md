# **Troubleshooting Cookbook**
Random collection of stuff I can't remember, thoughts and findings throughout my various troubleshooting voyages.

# **Systemd**

# **TLS**

## Viewing a websites TLS certificate
There are freely available TSL/SSL certificate tools online as well as inspection tools built into modern web browsers. To quickly verify the status of a websites TLS cert via the command line, use the `openssl` command.

- `openssl s_client -connect example.com:443`

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



