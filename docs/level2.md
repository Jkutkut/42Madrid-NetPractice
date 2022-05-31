# Level 2:

## Goal 1:
- Client B: mask invalid (32 mask does not allow 222). It should be 224.
- Client A: The first 3 bits can not be modified (see Mask). Having in mind B's IP, the first 3 bits are 101.
	- Any number following that should be valid (221).

### My calculations:

128    64    32    16    8    4    2    1    |  Number
  1     1     1     0    0    0    0    0    |    224
  1     1     0     1    1    1    1    0    |    222
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0

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

