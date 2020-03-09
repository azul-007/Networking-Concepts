## 1. How many subnets? 2^x = number of subnets. X is the number of masked bits or 1s.
**Example:** 11000000. The number of 1s is two, so 2^2 = 4 subnets.

## 2. How many hosts per subnet? 2^y - 2 = number of hosts per subnet.
**Example:** Y is the number of unmasked bits or 0s. For example, 11000000, the number
of 0s gives us 2^6-2 = 62 hosts per subnet. Substract to 2 for the subnet
and broadcast address.

## 3. What are the valid subets? 256 - subnet mask = block size
**Example:** 256 - 192 = 64. The block size of a 192 mask is always 64. Start
counting at zero in blocks of 64 until you reach the subnet mask value, and these
are your subnets. 0, 64, 128,192.

## 4. What's the broadcast address for each subnet? Because we counted our subnets in the 
## last section as 0, 64, 128, 192, the broadcast address is always the number to the right before the next subnet.
**Example:** The 0 subnet has a broadcast of 63 because the next subnet is 64. The 64 subnet 
has a broadcast address of 127 because the next subnet is 128. Remember, the broadcast of the
last subnet is always 255.

## 5. What are the valid hosts? Valid hosts are the numbers between the subnets, omitting all the 0s and all the 1s. 
**Example:** If 64 is the subnet number and 127 is the broadcast address, then 65 - 126 is the
valid host range - it's always the numbers between the subnet address and the broadcast address.
