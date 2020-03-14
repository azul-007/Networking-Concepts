## Virtual LANS

A VLAN is a logical grouping of network users and resources connected to administratively defined ports on a switch. When you create VLANs, you gain the ability to create smaller broadcast domains within a Layer 2 switched internetwork by assigning the various ports on the switch to different subnetworks. A VLAN is treated like its own subnet or broadcast domain, meaning that frames broadcasted onto the network are only switched between the ports logically grouped within the same VLAN.

If you want inter-VLAN communication, you will still need a router.

# VLAN Basics
The below image depicts how Layer 2 switched networks are typically designed - as flat networks. With this configuration, every broadcast packet transmitted is seen by every device on the network regardless of whether the device needs to receive that data or not.

![](https://github.com/azul-007/Networking-Concepts/blob/master/Images/flat_network.jpg)
