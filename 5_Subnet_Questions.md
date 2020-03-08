## 1. How many subnets? 2^x = number of subnets.
X is the number of masked bits or 1s.
For example, 11000000. The number of 1s is two, so 2^2 = 4 subnets.

## 2. How many hosts per subnet? 2^y - 2 = number of hosts per subnet.
Y is the number of unmasked bits or 0s. For example, 11000000, the number
of 0s gives us 2^6-2 = 62 hosts per subnet. Substract to 2 for the subnet
and broadcast address.
