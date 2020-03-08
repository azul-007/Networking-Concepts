# Address Resolution Protocol

Address Resolution Protocol finds the hardware address of a host from a known IP address. When IP has a datagram to send, it must inform a Network Access protocol of the destinations hardware address on the local network. If IP doesn't find the destination host's hardware address in the arip cache, it uses ARP to find this information.

ARP interrogates the local network by sending out a broadcast asking the machine with the specified IP address to reply with its hardware address.

![](https://github.com/azul-007/Networking-Concepts/blob/master/Images/ARP.jpg)
