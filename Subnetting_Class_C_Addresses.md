# Practice Example 1C: 255.255.255.128/25
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
