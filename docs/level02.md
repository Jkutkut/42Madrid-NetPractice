# Level 2:

## Goal 1:
- Client B: mask invalid (32 mask does not allow 222). It should be 224.
- Client A: The first 3 bits can not be modified (see Mask). Having in mind B's IP, the first 3 bits are 101.
	- Any number following that should be valid (221 = 11011101).

## Goal 2:
- The Masks given with the format /XX follow this rule:
	- There're 32 bits on a IP v4.
	- If 30 is given => there're 32 - 30 = 2 '0s'
	- Therefore, the mask is 11111111 ... 11111100
- 127.0.0 = localhost
- As long as you follow the Mask, the IPs can have "any" value
### My calculations:

128    64    32    16    8    4    2    1    |  Number
  1     1     1     0    0    0    0    0    |    224
  1     1     0     1    1    1    1    0    |    222
  1     1     1     1    1    1    0    0    |    252
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0




252
126 0
63 0
31 1
15 1
7 1
3 1
1 1
1

224
112 0
56 0
28 0
14 0
7 0
3 1
1 1
1


222
111 0
55 1
27 1
13 1
6 1
3 0
1 1
1

