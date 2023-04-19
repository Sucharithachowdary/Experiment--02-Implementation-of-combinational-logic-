# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 ~~~
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
 ~~~

## Logic Diagram
~~~
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.
~~~
## Procedure
~~~
The input and output variables are allocated with letter symbols. The exact truth table that defines the required relationships between inputs and outputs is derived. The simplified Boolean function is obtained from each output. The logic diagram is drawn.
~~~
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: sucharitha.k
RegisterNumber:  212221240021
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: R.HEMAPRIYA
RegisterNumber: 212221230043 
*/

module ff(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);
endmodule

module de (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule
*/


## Output:
## RTL
![233140197-b0ac2a7a-3a68-4b22-9fa4-f32238714772](https://user-images.githubusercontent.com/94166007/233160596-ecae9cb4-aae7-41b2-9988-6d358e59eab7.png)
![233140481-3ed8d231-7a75-4f40-8e22-d4138dfabd83](https://user-images.githubusercontent.com/94166007/233160651-23c4c12f-4b35-42ea-93d8-1c0a2867c83a.png)

## Timing Diagram
![233140767-d3d8b21b-e6b0-43f4-9bd8-45a5d0b74985](https://user-images.githubusercontent.com/94166007/233160700-16534e07-a08d-440f-8c46-640629e69edc.png)
![233140873-7766925f-1d86-4e18-955f-37faf76323a6](https://user-images.githubusercontent.com/94166007/233160724-f9f6dd40-0667-430e-a2fe-12fb9725a610.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
