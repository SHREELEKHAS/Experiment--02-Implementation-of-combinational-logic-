# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:

 Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime


## Theory:
 A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.

## Program:
``` 
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: SHREE LEKHA.S
RegisterNumber:  23014046
*/
module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule
``` 

## OUTPUT:
## Truth Table:
![output](/Verilog1/truth_table_abcd.png)

![output](/Verilog1/truth_table_wxyz.png)

## RTL realization:
![output](/Verilog1/circuit_diagram.png)
## Timing Diagram:
![output](/Verilog1/waveform.png)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
