## 1 Practice Example 1C: 255.255.255.128/25
## Because 128 is 10000000 in binary, there is only 1 bit for subnetting, and there are 7 bits for hosts. We're giong to subnet the Class C network address 192.168.10.0

Network Address = 192.168.10.0
Subnet Mask     = 255.255.255.128

1. How many subnets? 2^x
128 = 10000000. Count the ones...2^1 = 2 subnets

2. How many hosts per subnet? 2^y - 2
128 = 10000000. Coun the zeros...2^7-2 = 126 subnets

3. What are the valid subnets? 256 - 128. Remeber to start at zero and count in our block size.
Our subnets are 0, 128

4. What's the broadcast address for each subnet?
For the 0 subnet, the next subnet is 128, so the broadcast of the 0 subnet is 127.

5. What are the valid hosts?
* Subnet: 0
* First host: 1
* Last host: 126
* Broadcast: 127

* Subnet: 128
* First host: 129
* Last host: 254
* Broadcast: 255


## 2 Practice Example 2C
## In this second example, we're going to subnet the network address 192.168.10.0 using the subnet mask 255.255.255.192.

Network address = 192.168.10.0
Subnet Mask = 255.255.255.192

1. How many subnets? 2^x
192 = **11**000000. Count the ones, 2^2 = 4 subnets

2. How many hosts per subnet? 2^y-2
192 = 11**000000**. Count the zeros, 2^6-2 = 62 hosts

3. What are the valid subets? 256 - subnet mask
256 - 192 = 64. Valid subnets are 0, 64, 128, 192. Remember to count up to the subnet mask

4. What's the broadcast address of each subnet?
* 0 subnetmask, broadcast is 63
* 64 subnetmask, broadcast is 127
* 128 subnetmask, broadcast is 191
* 192 subnetmask, broadcast is 255

5. What are the valid hosts for each subnet?
* **Subnet: 0
* First Host: 1
* Last Host: 62
* Broadcast: 63

* **Subnet: 64
* First Host: 65
* Last Host: 126
* Broadcast: 127

* **Subnet: 128
* First Host: 129
* Last Host: 190
* Broadcast:191

* **Subnet: 192
* First Host: 193
* Last Host: 254
* Broadcast: 255




## 3 Practice Example 3C
## Subnet the network address 192.168.10.0 and subnet mask 255.255.255.224

Network Address: 192.168.10.0
Subnet Mask: 255.255.255.224

1. How many subnets? 2^X
11100000 = 224. Count the 1s. 2^3 = 8 subnets

2. How many hosts? 2^Y - 2
Count the zeros. 2^5 - 2 = 30 hosts.

3. What are the valid subnets? 256 - subnet mask
256 - 224 = 32 valid hosts. Remember to start at 0 and count in blocks to the subnet mask value
0,32,64,96,128,160,192,224

4. What's the broadcast address
**Subnet Mask:0
* First Valid Host: 1
* Last Valid Host: 30
* Broadcast: 31

* Subnet Mask: 32
* First Valid Host: 33
* Last Valid Host:62
* Broadcast:63

* Subnet Mask: 96
* First Valid Host: 97
* Last Valid Host: 126
* Broadcast: 127

* Subnet Mask: 128
* First Valid Host: 129
* Last Valid Host: 158
* Broadcast: 159

* Subnet Mask: 160
* First Valid Host: 161
* Last Valid Host: 190
* Broadcast: 191

* Subnet Mask: 224
* First Valid Host: 225
* Last Valid Host: 254
* Broadcast: 255
