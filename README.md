# IpMac
Internet Protocol using configurable MAC address

# Facts
32bits IPv4 is too small for an 8 gigahumans planet.

128bits IPv6 is not loved.

48bits MAC address are now configurable on all equipment.

# Proposal
Lets use 48bits IP address stored in MAC address!

0.0.x.x.x.x will be the legacy internet for compatibility and non breaking migration.

0.0.127.0.0.1 will be the local host.

0.0.192.168.x.x, 0.0.172.16.x.x and 0.0.10.x.x.x , will be private lans.

# Consequences
Switches are still working fine without modification.

ARP become useless.

Vlan are still working the same way.

We need a new ethertype.

Routeur/OS need to be able to manage the new IpMac protocole.

After migration all 0.0.x.x.x.x will be private lan.

After migration we gain 64bits of src and dst IP address for IP data.

## NAT?

No more needed after full migration.

## Firewall

Easy to adapte.

# DHCP?



## What else?


