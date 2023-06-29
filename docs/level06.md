# Level :

## Goal 1:
### A -> I
- Mask A1: S is a switch. Therefore, R1 and A1 are on the same network (**IMPORTANT**).
	- Therefore: Mask A1 = Mask R1 = `255.255.255.128`
- IP R1: Same network as A1 => Compatible with A1 => `68.62.255.254` is valid IP.
- Client A: `0.0.0.0/0 => IP R1`
	- Anything not on this network must go through R1.
- Router R: To go to I, we go to `8.8.0.0/16` usign the given 163.172.250.1

### A -> I:
- internet I: `IP A1 => 163.172.250.12`
WHY?
- If you are on I, you need to change network to go to A1.
	- Therefore, intenet I needs those values.
- When reaching R, the wanted IP is checked (IP A1). That IP is on a known network. Therefore, there is no problem => go through R1.
- Rest of the forwarding is trivial.

### My calculations:


128    64    32    16    8    4    2    1    |  Number
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0
  0     0     0     0    0    0    0    0    |    0


240 | 0
120 | 0
60  | 0
30  | 0
15  | 1
7   | 1
3   | 1
1


