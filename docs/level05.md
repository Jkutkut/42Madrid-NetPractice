# Level :

## Goal 1:
- We need to connect A with router using R1.
- Because of R1 Mask and IP, we can use any IP for A with first bit 0 and same Mask

## Goal 2:
- Mask ...192.0 => 8 + 6 = 14 => 32 - 14 = 18 => /18
- For that reason, 170.122.XX.XX (170.122.42.42) is valid if you follow 192

## Goal 3: XXXXXXX => YYYYYYY
### A to B:
- If you want to go to B, you need to go through the router.
	- Therefore, YYYYYYY = R1's IP.
	- XXXXXXX is composed of a DIR/MASK.
		- MASK: 255.255.192.0 => /18 (see Goal 2)
		- Because of the mask, any value between 170.122.63.255 and 170.122.0.0
			- Why? If you give both, all the IPs can be inferred.
	- Therefore: 170.122.63.255/18 => 73.245.168.126 WORKS.
	- Therefore: 170.122.0.0/18 => 73.245.168.126 WORKS.

### B to A:
- Same logic:
	- Default means any dir not found? TODO
	- YYYYYY = R2's IP

### My calculations:


128    64    32    16    8    4    2    1    |  Number
  0     1     1     1    1    1    1    0    |    126
  1     1     0     0    0    0    0    0    |    192
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0

