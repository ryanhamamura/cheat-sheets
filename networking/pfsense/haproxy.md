## Install required packages
1. Acme
2. Haproxy

## Move web GUI TCP Port away from 443
Under `System > Advanced > Admin Access`, change the TCP port from 443 to
something else like 10443. Also disable WebGUI redirect so that pfsense will
stop listening on port 80. 

## `System > Acme Certificates > General Settings`
Enable Acme cron job for client renewal

## `Services > Acme > Account keys`
Create new account key 
```
Name: 
Description: 
ACME Server:
    1. Let's Encrypt Staging ACME v2 (for testing)
    2. or if ready for production, Let's Encrypt Production ACME v2
Generate new account key
Register account key once the key field is populated
Save
```
