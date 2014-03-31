ansible-role-tinyproxy
======================

Ansible host for configure Tinyproxy


# Examples

## Run local tinyproxy with forbidden websites
```
     - role: tinyproxy
       tinyproxy_filters: 
          - forbidden.com
          - .otherforbiddenwebsite.com

```

## Run tinyproxy  on localnetwork with whitelist websites
```
     - role: tinyproxy
       tinyproxy_filterDefaultDeny: "Yes"
       tinyproxy_listen: "192.168.0.1"
       tinyproxy_filters: 
          - ftp.free.fr
          - security.ubuntu.com
          - .archive.ubuntu.com
       tinyproxy_allows:
          - 127.0.0.1
          - 192.168.0.1/24

```
