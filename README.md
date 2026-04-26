# IPv5
Internet Protocol using configurable MAC address to suppress ARP overhead.

# IPv4 optimization
I don't understand why ARP is still existing nowdays while all ethernet card have configurable MAC... just set it to 0.0.IP.IP.IP.IP and everybody knows your MAC address.

As MAC are 48bits, we could also extend IP to 48 bits and forget the IPv6 mess...


# Facts
32bits IPv4 is too small for an 8 gigahumans planet.

128bits IPv6 is not loved.

48bits MAC address are now configurable on all equipment.

# Proposal
Lets use 48bits IP address and configure MAC address the same to suppress ARP overhead!

0.0.x.x.x.x will be reserved for the legacy internet. It will allow IPv4 encapsulation for easy migration.

IPv4 part of the network still work as before, with traditional MAC.

Two IPv4 can communicate across an IPv5 Internet because routers just need to add or remove the 0.0. beginning of the address.

IPv4 clients can't reach IPv5 only servers.

IPv5 clients can't reach IPv4 only servers.

# Consequence

if eth0 have IP `1.2.3.4.5.6`, then it's MAC address is `01:02:03:04:05:06`, no need to broadcast everybody `who-is 01:02:03:04:05:06`.

When you want to reach an IP outside you LAN, just send it to the routeur using its obvious MAC = IP.

The paquet travel on Internet and the last routeur managing the target IP LAN, can use the same MAC = IP property to deliver the packet.

0.0.127.0.0.1 is the new localhost.

0.0.192.168.x.x, 0.0.172.16.x.x and 0.0.10.x.x.x , are the new private lans.

Switches are still working fine without layer 2 modification.

ARP become useless.

Vlan are still working the same way.

Routeur/OS need to be able to manage the new IPv5 protocol and IPv4 encapsulation.

After IPv4 death, all 0.0.x.x.x.x will become private lan.

MAC address economy collapse, all new IPv5 only equipment are using 0.0.0.0.0.0 by default.

IP address economy collapse.

## NAT?

No more needed after full migration.

## Firewall

Easy to adapte.

# DHCP?

request via ethernet broadcast + self generated public key.

reply via ethernet broadcast + public key encrypted IPv5 address and ack token.

ack from proposed IPv5 address + private key encrypted ack token.

Possible to accept only known pub key.

# bonding/LACP
Work the same...

# DNS
Should reply IPv4 or IPv5 address depending of the IP protool used for asking.

# is the name free?
https://hackaday.com/2025/03/09/ipv4-ipv6-hey-what-happened-to-ipv5/

## What else?
https://www.reddit.com/r/networking/comments/1sungvg/what_if_new/

