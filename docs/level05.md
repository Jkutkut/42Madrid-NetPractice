# Level :

## Goal 1:
- We need to connect A with router using R1.
- Because of R1 Mask and IP, we can use any IP for A with first bit 0 and same Mask

## Goal 2:
- Mask ...192.0 => 8 + 6 = 14 => /14
- For that reason, 170.122.XX.XX (170.122.42.42) is valid if you follow 192

## Goal 3:


### My calculations:


128    64    32    16    8    4    2    1    |  Number
  0     1     1     1    1    1    1    0    |    126
  1     1     0     0    0    0    0    0    |    192
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0

