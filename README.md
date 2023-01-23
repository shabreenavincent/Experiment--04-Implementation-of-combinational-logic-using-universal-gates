# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

Logic Diagram Procedure Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

PROGRAM 1:

module expfour(a,b,c,d,f);

input a,b,c,d;

output f;

wire f1,f2,f3;

assign f1 = (~c&~b&~a);

assign f2 = (~d&~c&~a);

assign f3 = (c&~(~b)&~a);

assign f= f1&~f2&~f3;

endmodule

PROGRAM 2:

module expfourtwo(a,b,c,d,f);

input a,b,c,d;

output f;

wire f1,f2,f3,f4;

assign f1 = c&(~b)&a;

assign f2 = d&(~c)&a;

assign f3 = c&(~b)&a;

assign f4 = ~(f1|f2|f3);

not(f,f4);

endmodule

RTL REALIZATION

OUTPUT

PROGRAM 1
![output program 1](https://user-images.githubusercontent.com/119475721/213979190-c6aebb13-9309-44b1-9130-47427730830d.png)


PROGRAM 2
![output program 2](https://user-images.githubusercontent.com/119475721/213979475-cd934f16-874a-4f93-93dd-eea7b55fa645.png)

Developed by: shabreenavincent
RegisterNumber:22009378

TRUTH TABLE

PROGRAM 1
![program 2](https://user-images.githubusercontent.com/119475721/213980331-794c64ff-99f9-42a9-87b4-8b982a38e9f0.png)





PROGRAM 2

![truthtable progarm 2](https://user-images.githubusercontent.com/119475721/213979784-7b69fed1-25ae-4f81-a030-9a37fbce71cb.png)





TIMING DIAGRAM

PROGRAM 1





![timing diagram program 1](https://user-images.githubusercontent.com/119475721/213979877-08b1d228-a5bb-4cd5-a9b4-c01ffcc38de2.png)


PROGRAM 2




![truthtable progarm 2](https://user-images.githubusercontent.com/119475721/213979913-c66d9d60-f128-4ec7-a2a0-2462c6d00215.png)

Result: 
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.





