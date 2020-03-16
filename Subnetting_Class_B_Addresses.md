# Use the same subnet numbers for the third octet with Class B that you used for the fourth octet with Class C, but add a 0 to the network portion and a 255 to the broadcast section in the fourth octet.

## Practice Example #1B: 255.255.128.0 /17
Network Address: 172.16.0.0
Subnet Mask: 255.255.128.0

1) Subnets? 2^x 128 = 10000000. 2^1 = 2
2) Hosts? 2^y-2, 2^15-2
3) Valid Subnets? 256-128=128. 0, 128.
Remember that subnetting in Class B starts in the third octet, so the subnet numbers are really 0.0 and 128.0. These are the exact numbers we used with Class C; we use them in the third octet and add a 0 in the fourth octet for the network address.

![](https://github.com/azul-007/Networking-Concepts/blob/master/Images/subnetting.jpg)

