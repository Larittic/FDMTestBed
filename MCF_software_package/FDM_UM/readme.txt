The format of input:

e.g. testcase_um_0.txt

// number of ship and satellite
5 3
// host number of each ship
4 3 5 4 4   

// connection between ships and satellites
1 0 1
1 1 0
0 1 1
1 1 0
1 0 1

// number of MPTCP requests
10
// src ship, dest ship, request BW
0 3 6
0 4 4
1 0 7
1 2 3
2 1 4
2 3 4
3 1 3
3 2 3
4 0 3
4 3 3

// number of UDP requests
5
// src ship, dest ship, request BW
0 2 4
2 0 2
2 4 5
3 1 6
4 3 3

// uplink capacities (n_ship x n_sat)
-1 0 -1
-1 -1 0
0 -1 -1
-1 -1 0
-1 0 -1

// satellite capacities
40 35 30

// downlink capacities (n_sat x n_ship)
-1 -1 0 -1 -1
0 -1 -1 -1 0
-1 0 -1 0 -1


The format of output:
Almost the same as original FDM, except every flow will be followed by its type.

e.g. allocation_0.txt

s5-eth7 s6-eth4	num_of_flow:3
		10.0.19.0 3 UDP
		10.0.18.0 3 MPTCP
		10.0.17.0 0.873501 MPTCP


P.S.
input: testcase_um_0.txt
output: allocation_0.txt
The total flow at the 3 satellites are:
23.598/40
20.4402/35
15.9618/30