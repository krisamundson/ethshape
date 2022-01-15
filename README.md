# ethshape

Linux traffic shaper for ethereum geth and prysm beacon-chain

# configure

- Change the `INTERFACE` var to the network interface ethereum traffic uses.
- Change the `BANDWIDTH_LIMIT` to preference, default is 3 Mbps.

# details

- geth/prysm ports are limited to combined `BANDWIDTH_LIMIT` in class 1:10
- FQ_Codel within class 1:10
- all other traffic into default class 1:20
- Class 1:10 == high priority but bandwidth limited
- Class 1:20 == default and full rate (GigE NIC)

# more information

- [Fair Queuing with Controlled Delay](https://www.man7.org/linux/man-pages/man8/tc-fq_codel.8.html)
