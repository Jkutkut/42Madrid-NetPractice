# Level 4:

- mac = /23 => 255.255.254.0
- A's IP = 70.9.118.132 => now we have the ips ideas
- Example: IPs from 132-134 work fine

- Therefore, also works with 255.255.255.128 as mask and ips 132-134

### My calculations:

/23 => 32 - 24 = 8 + 1


128    64    32    16    8    4    2    1    |  Number
  1     0     0     0    0    0    0    0    |    128
  1     1     0     0    0    0    0    0    |    192
  1     1     0     0    1    0    0    0    |    132
  0     0     0     0    0    0    0    0    |    0


192
96 0
48 0
24 0
12 0
6 0
3 0
1 1
1

132 0
66 0
33 0
16 1
8 0
4 0
2 0
1 0
1



