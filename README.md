# IPv5
Internet Protocol using configurable MAC address

# Facts
32bits IPv4 is too small for an 8 gigahumans planet.

128bits IPv6 is not loved.

48bits MAC address are now configurable on all equipment.

# Proposal
Lets use 48bits IP address stored in MAC address!

0.0.x.x.x.x will be reserved for the legacy internet. It will allow IPv4 encapsulation for easy migration.

# Consequence

0.0.127.0.0.1 is the new localhost.

0.0.192.168.x.x, 0.0.172.16.x.x and 0.0.10.x.x.x , are the new private lans.

Switches are still working fine without modification.

ARP become useless.

Vlan are still working the same way.

We need a new ethertype.

Routeur/OS need to be able to manage the new IPv5 protocol and IPv4 encapsulation.

After migration all 0.0.x.x.x.x will become private lan.

we gain 64bits from src and dst IPv4 address for IP data.

MAC address economy collapse, all equipment are using 0.0.0.0.0.0 by default.

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
Shoul reply IPv4 or IPv5 address depending of the IP protool used for asking.

## What else?


