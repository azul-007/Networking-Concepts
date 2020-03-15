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

# Concerns!
* What happens if the hub for Sales is full and we need to add another user to the Sales LAN?
* What do we do if there's no more physical space for a new employee where the Sales team is located?

Why not just plug the Sales team member into the Finance hub? 

# Security Issues
* Because the new Sales employee is a member of the Finance broadcast domain, he newbie can see all the same servers and access all network services that the Finance ppl can.
* For this user to access the Sales network services they would have to go through the router to log in to the Sales server. 

# What does a Switch accomplish for us?
The following image show how six VLANS (2-7) are used to create a broadcast domain for each department. Each switch port is then administratively assigned a VLAN membership

Now if we needed to add another user to the Sales VLAN, we could just assign the port to VLAN 7 regardless of where the new Sales team member is physically located.

VLAN 1 is not depicted because it is an administrative VLAN . All ports on a switch are members of VLAN 1 until you change them.

The hosts within each VLAN can communicate with each other but not with anything in a different VLAN because the hosts in any given VLAN "think" that they're actually in a collapsed backbone.

A router or any Layer 3 device must be used for communication between VLANs. 
