# **Troubleshooting Cookbook**
Random collection of stuff I can't remember, thoughts and findings throughout my various troubleshooting voyages. Most of the commands here will be nix based. Callouts to Windows commands will be provided where necessary.

## Website triage
<p>When looking into website problems there are many different tools to use to gather information and debug common issues.</p>

## Systemd

## TLS
<p>TLS is the successor to SSL and is used to secure (encrypt) client connections to web servers.</p>

### Viewing a websites TLS certificate
<p>There are freely available TSL/SSL certificate tools online as well as inspection tools built into modern web browsers.</p> 

<p>To quickly verify the status of a websites TLS cert via the command line, use the <strong>openssl</strong> command.</p>

<p>You can gather up the following information using openssl command:</p>

<ul>
  <li>TLS certificate chain details</li>
  <li>Server certificate (public)</li>
  <li>SSL/TLS Handshake</li>
  <li>Supported TLS version</li>
  <li>Supported ciphers</li>
</ul>

<p><strong>openssl s_client -connect example.com:443</strong></p>

<p>Output Example (truncated for readability):</p>

```
$ openssl s_client -connect example.com:443
Connecting to 93.184.216.34
CONNECTED(00000006)
depth=2 C=US, O=DigiCert Inc, OU=www.digicert.com, CN=DigiCert Global Root G2
verify return:1
depth=1 C=US, O=DigiCert Inc, CN=DigiCert Global G2 TLS RSA SHA256 2020 CA1
verify return:1
depth=0 C=US, ST=California, L=Los Angeles, O=Internet Corporation for Assigned Names and Numbers, CN=www.example.org
verify return:1
---
Certificate chain
...
---
Server certificate
-----BEGIN CERTIFICATE-----
```

## Firewalls

### ufw
<p>Uncomplicated firewall, acts as a wrapper for iptables and is usually installed by default on Ubuntu distributions.</p>

### ufw commands
- `sudo ufw enable` - turns ufw on
- `sudo ufw status verbose`
- `sudo ufw status numbered` - show order of rules
- `sudo ufw allow <service name>`
- `sudo ufw allow from <ip> to port <port>`
- `sudo ufw allow from <ip> to port <port> proto <protocol>`
- `sudo ufw deny from <ip or subnet> to any port <port>`
- `sudo ufw delete <rule number>`
- `sudo ufw insert <rule number> allow from <ip>`

### iptables
One of the OGs for OS level firewall rules on Linux systems. 


### firewalld

###



