### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![diagram1](https://github.com/maaplasai7/ex.2/assets/134155273/cd493e36-ed70-42af-9b7e-821cfdefb905)
![diagram2](https://github.com/maaplasai7/ex.2/assets/134155273/062cf191-7b82-4e2f-8bdd-e9d40be45d6a)


## Truth Table:
![truth 1](https://github.com/maaplasai7/ex.2/assets/134155273/6c564020-e86b-40ed-afb3-79364e68c05c)


## Program:
~~~
module exp2a(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
~~~



## RTL Schematic:
![exp2 RTL](https://github.com/maaplasai7/ex.2/assets/134155273/41deada5-b62c-403c-bdc3-fffcfb829ce3)




## Timing Diagram:
![exp2 Timiing Diagram](https://github.com/maaplasai7/ex.2/assets/134155273/2382a73b-315f-495c-bfd9-548ccbcfdb98)




## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



