# Level 8:

**Important**: internet I is the key!

We have 142.182.95.0/26 and must be divided into 3 subnets:

1 -> 00 -> 00000000 -> 0
2 -> 01 -> 00010000 -> 16
3 -> 10 -> 00100000 -> 32
4 -> 11 -> 00110000 -> 48

Mascara: 255.255.255.240 -> /28
	- Take a look at D1's mascara: 240! Exacly /28 => Correct subnetworking.

- All internal masks: /28
- internet I: It must connect to R12 => `142.182.95.0/26 => 163.33.250.12`

We have the restriction in R2: It routes the trafic from D and C to 142.182.95.62.
Therefore:
- R13: 142.182.95.62/28
That makes R21 also be in the 4th network
- R21: 142.182.95.61/28
Now, we can route all trafic from I to R21, while the rest goes to I:
- Router R1:
	- `default => 142.182.95.61`
	- `0.0.0.0/0 => >163.33.250.1`
- Router R2: We want all traffic forwarded to R13, so use default.
Just take 2 remaining networks and apply them to the remaining.

- R23: 142.182.95.20/28
- D1: 142.182.95.25/28 (255.255.255.240)
- client D: `default => 142.182.95.20`
- R22: 142.182.95.1/28
- C1: 142.182.95.2/28
- client C: `0.0.0.0/0 => 142.182.95.1`

## Goal 1:


## Goal 2:
## Goal 3:


### My calculations:


128    64    32    16    8    4    2    1    |  Number
  1     1     1     1    0    0    0    0    |    240
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0

