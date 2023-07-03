# Level :

## Goal 1:
Divide network into, at least, 3 subnets.
The amount of subnetworks is the min power of 2 greater 3 => 2^2 = 4

If we supose the network is 107.198.14.0/24:

1 -> 00 -> 00000000 -> 0
2 -> 01 -> 01000000 -> 64
3 -> 10 -> 10000000 -> 128
4 -> 11 -> 11000000 -> 192

Mascara: 255.255.255.192 -> /26

Therefore:

- If we look a R11 and R12, those must be the networks 1 and 4. There aren't any other restrictions so let's use the network 2 for the R22-C subnetwork.

- All masks: /26
- A1: 107.198.14.2 (or any other in that subnetwork).
	- client A: `default -> 107.198.14.1` (all to the router R).
- C1 and R22: same logic. Network 2 => any IP in range is valid
	- C1: 107.198.14.66
	- R22: 107.198.14.65
	- Client C: `default -> 107.198.14.65`
- R21: If you look at ranges, 107.198.14.193 is valid IP.
- R1: All in subnet 2, go to R21:
	`107.198.14.64/26 -> 107.198.14.193`
- R2: All in subnet 1, go to R12:
	`107.198.14.0/26 -> 107.198.14.254`

### My calculations:


128    64    32    16    8    4    2    1    |  Number
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0

