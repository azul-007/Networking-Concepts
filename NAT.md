# Network Address Translation
Network Address Translation (NAT) is a process in which one or more local IP address is 
translated into one or more Global IP address and vice versa in order to provide Internet 
access to the local hosts. You would typically use NAT on a border router.

Here are a list of situations when it's best to have NAT:
- You need to connect to the Internet and your hosts don't have globally unique IPs.
- You change to a new ISP that requires you to remember your network.
- You need to merge two intranets with duplicate addresses.

Types of Network Address Translation

## Static NAT
Allows one to one mapping between local and global addresses. 

## Dynamic NAT
Allows mapping of an unregistered IP address to a registered IP address from a pool of registered IP addresses.
You don't have to statically configure your router to map an inside-to-an-outside-address as you would using static
NAT.

## Overloading
Overloading is a form of dynamic NAT that maps multiple unregistered IP addresses to a single registered IP address
many to one -- using different ports.

## NAT Names
Addresses used after NAT translations are called global addresses. These are usually the public addresses used on the internet.
Inside local addresses are actually the private address of the sending host that's trying to get to the Internet, while the
outside local address is the address of the destination host.
