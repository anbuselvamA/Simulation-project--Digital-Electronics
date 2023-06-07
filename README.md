# TITTLE
To Design and simulate 2 bit synchronous upcounter with JK flip flop using Verilog

# THEORY
Synchronous Counters: It means that all flip-flops are clocked concurrently. The clock pulses drive the clock input of each flip-flop together hence there is no propagation delay.

2 bit counter Synchronous Counter: This have five counter states. The counter design table for such counter shows the three flip-flop and their states also (0 to 5 states), as in table (a), the 6 inputs needed for the three flip-flops. The flip-flop inputs needed to step up the counter from the current to the next state have been worked out along with the assist of the excitation table illustrated in the table.

# LOGIC DIAGRAM
![image](https://github.com/anbuselvamA/Simulation-project--Digital-Electronics/assets/119559871/2caad0a0-3693-48d3-b5ec-a7009c0d5690)


# NETLIST DIAGRAM
![image](https://github.com/anbuselvamA/Simulation-project--Digital-Electronics/assets/119559871/04197f3d-b788-44a3-a822-458fc467777a)


# TIMING DIAGRAM
![image](https://github.com/anbuselvamA/Simulation-project--Digital-Electronics/assets/119559871/a3213d86-4044-4258-8dfa-f6526507a795)


# PROGRAM

```
module 2 bit counter(q, qbar, j, k,clk, rst, pr);
output [2:0] q, qbar;
input clk, j, k;
input rst, pr;
wire a;
nand n1(a,q[1],q[2]);
JKFF_Pos_Edge jkff0(q[o],
qbar[0],j,k,clk,a,pr);
JKFF_PoS_Edge jkff1 (q[1],
qbar[1],j,k,qbar[0],a,pr);
JKFF_PoS_Edge jkff3(q[2],
```
# REFERENCE
