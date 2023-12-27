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



Write the detailed procedure here 


## Program:
  ```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Rogith gansh.R
RegisterNumber:  212223100046
```
## half subtractor
```
module half_sub(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor (difference,a,b);
not (x,a);
and (borrow,x,b);
endmodule
```
## full subtractor
```
module Full_sub(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
wire p;
assign difference=((a^b)^bin);
not (p,a);
assign borrow=((p&b)|(p&bin)|(b&bin));
endmodule
```
## Truthtable
# half subtractor
![image](https://github.com/ROGITHGANESH/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152588322/6392cb46-a57e-454d-a21a-670ba25e8a3e)
# full subtractor
![image](https://github.com/ROGITHGANESH/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152588322/8cc209ca-dd80-4f7e-9dd5-f32c5ddb9437)

##  RTL realization
## half subtractor
![image](https://github.com/ROGITHGANESH/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152588322/1434db22-b185-41a7-80a2-fa205d624e9a)

## full subtractor
![image](https://github.com/ROGITHGANESH/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152588322/66a9f4b6-4f37-4ae3-9c7e-70d0bfac232b)

## Timing diagram 
## half subtractor
![image](https://github.com/ROGITHGANESH/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152588322/a18a6ea3-72b9-4752-a4ae-a1e7dbc24d6a)

## full subtractor
![image](https://github.com/ROGITHGANESH/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152588322/ccd62d00-bb98-4740-a46f-2cff14302f97)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
