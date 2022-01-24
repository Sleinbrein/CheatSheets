# Linux

## Debian
Change networkinterfaces
```bash
sudo vim /etc/network/interfaces
```
Activate/disable interface
```bash
ifup eth1
ifdown eth0
```

## Red Hat
Change networkinterfaces
```bash
cd /etc/sysconfig/network-scripts/
sudo vim ifcfg-eth1
```

## Global
Bash script template
```bash
#!/bin/bash
# ------------------------------------------------------------------
# [Author] Niels Van Dorpe
# [Description]
# ------------------------------------------------------------------

set -o errexit   # abort on nonzero exitstatus
set -o nounset   # abort on unbound variable
set -o pipefail  # don't hide errors within pipes
```

Copy file from another VM to host VM
```bash
scp vagrant@192.168.76.72:/home/vagrant/testbestand /home/osboxes/Documents/
```
