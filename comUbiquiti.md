# Ubiquiti

SSH into server address
  The SSH user account name is root@server-address
  password is under UDM-Pro settings SSH password
  Type help to see commands

VPN Apple/SystemPrefences/Newtork
  Create new
    Type L2TP (iOS)
    Server domain.com
    account/username: UDM-Pro/Network/Settings/Gateway/RADIUS/ Users
    User password: above user password
    Shared Secret/secret: RADIUS secret password
    Advanced: Check send all traffic through VPN

- UniFi VPN server
  - Ubiquiti VPN with Dynamic IP
  - [help options](https://jkindon.com/2020/04/14/azure-and-ubiquiti-vpn-with-dynamic-ip-address/)
  - [help options](https://help.ui.com/hc/en-us/articles/360015268353-UniFi-USG-UDM-Configuring-RADIUS-Server)
  - [help options](https://help.ui.com/hc/en-us/articles/115005445768-UniFi-USG-UDM-Configuring-L2TP-Remote-Access-VPN)

- [Config namecheap for DNS](https://www.namecheap.com/support/knowledgebase/article.aspx/43/11/how-do-i-set-up-a-host-for-dynamic-dns)

- [Configuring Ubiquiti UniFi USG to use Namecheap DDNS](https://daltonf.com/configuring-ubiquiti-unifi-usg-for-namecheap-ddns/)

Service: namecheap

Hostname: If you're using a subdomain, this is the first segment (ex. for house.your-home-server.com, use house here). If you're using the top-level domain (ex. "your-home-server.com"), put *

Username: For Namecheap, this is the top level domain with no subdomain (ex. your-home-server.com). Other DDNS services may give you a specific username (ex. YOUR_DYNAMIC_DNS_PASSWORD)

Password: This is the password from the Namecheap settings (ex. YOUR_DYNAMIC_DNS_PASSWORD)

Server: I found this from other Namecheap tutorials:

dynamicdns.park-your-domain.com
