## Virtual LANS

A VLAN is a logical grouping of network users and resources connected to administratively defined ports on a switch. When you create VLANs, you gain the ability to create smaller broadcast domains within a Layer 2 switched internetwork by assigning the various ports on the switch to different subnetworks. A VLAN is treated like its own subnet or broadcast domain, meaning that frames broadcasted onto the network are only switched between the ports logically grouped within the same VLAN.

If you want inter-VLAN communication, you will still need a router.

# VLAN Basics
The below image depicts how Layer 2 switched networks are typically designed - as flat networks. With this configuration, every broadcast packet transmitted is seen by every device on the network regardless of whether the device needs to receive that data or not.

![](https://github.com/azul-007/Networking-Concepts/blob/master/Images/flat_network.jpg)

The reason it's called a flat network is because of it's one broadcast domain, not because the actual design is physically flat.

## Physical LANs Connected to a router
To understand how a VLAN looks to a switch, it's helpful to begin by first looking at a traditional network.
![](https://github.com/azul-007/Networking-Concepts/blob/master/Images/physical_lan.jpg)

* Each network is attached with a hub port to the router.
* Each host attached to a particular physical network has to match that network's logical network number in order to be able to communicate on the internetwork.
* Each department has its own LAN - to add them to the Sales department, plug them into the Sales LAN and they would automatically be part of the Sales collision and broadcast domain.
