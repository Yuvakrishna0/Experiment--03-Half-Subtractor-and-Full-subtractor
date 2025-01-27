# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1: Use module project name(input,output) to start the Verilog programmming.

2: Assign inputs and outputs using the word input and output respectively.

3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4: Use each output to represnt onre for differnce and the other for borrow.

5: End the verilog program using keyword endmodule.


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Yuva krishna k 
RegisterNumber: 212222110056 
*/
## HALF SUBRACTOR:
```
module learner(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```
## FULL SUBRACTOR:
```
module exp4fulladder(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&(b^c)|(b&c));
endmodule
```


## Truthtable

## HALF SUBRACTOR:
![266499748-209500d3-2760-482c-94c4-81c9c586dcd4](https://github.com/Yuvakrishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/117915037/116d2ca9-7af8-4ce7-bdaf-3ef3a67d807c)

## FULL SUBRACTOR:
![266499766-8511bcf6-c04d-43d2-a2a5-36bc079745dd](https://github.com/Yuvakrishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/117915037/9d7bf430-3678-4137-a996-ab92deeb50f4)


##  RTL realization
## HALF SUBRACTOR:
![266497007-1cc1a497-df76-415c-b20b-63f9dda5ca12](https://github.com/Yuvakrishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/117915037/1c99fbc7-6172-489d-9d96-3b022b994acb)
## FULL SUBRACTOR:
![266495473-4a073916-7b92-438d-acf3-7cb0ae95922b](https://github.com/Yuvakrishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/117915037/afad1a62-d10b-47c4-b771-cd6c53786325)


## Timing diagram :
## HALF SUBRACTOR:
![266498625-7a8b57e1-d724-4614-81f3-306f4e484793](https://github.com/Yuvakrishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/117915037/0a30fb6c-7856-4f6a-8c83-a6587d7e8e72)
## FULL SUBRACTOR:
![266497680-62a29b2d-52f6-486d-a1bc-c049b0a4f272](https://github.com/Yuvakrishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/117915037/cf91a8c1-8f85-4d77-a5f7-9fafd28fd8e8)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
