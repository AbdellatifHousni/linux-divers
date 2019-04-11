# linux-divers

## Netplan ID's with weird MAC Address in Windows DHCP Server
source : https://bugs.launchpad.net/netplan/+bug/1759532

### solution :
1) cp /run/systemd/network/10-netplan-ens160.network /etc/systemd/network/
2) update /etc/systemd/network/10-netplan-ens160.network to add in ClientIdentifier=mac under the [DHCP] section
3) systemctl restart systemd-network

