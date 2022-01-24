# Linux

## Debian
### Network
Change networkinterfaces
```bash
sudo vim /etc/network/interfaces
```

Activate/disable interface
```bash
ifup eth1
ifdown eth0
```

Restart networkmanager
```
sudo network-manager restart
```

### Firewall
Check firewall
```bash
sudo firewall-cmd --list-all
```
Add service to firewall
```bash
sudo firewall-cmd --add-service=http --permanent
sudo firewall-cmd 
sudo firewall-cmd --reload
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

Create RAID 5
```bash
# create fd partition on every disk
sudo fdisk /dev/sdc
# create RAID 5
sudo mdadm --create /dev/md0 --chunk=64 --level=5 --raid-devices=3 /dev/sdc /dev/sdd /dev/sde
```

Remove RAID 5
```bash
sudo mdadm --stop /dev/md0
```
