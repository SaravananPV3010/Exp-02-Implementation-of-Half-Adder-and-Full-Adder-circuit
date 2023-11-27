# Implementation-of-Half-Adder-and-Full-Adder-circuit
## Aim:
#### To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
#### Hardware – PCs, Cyclone II , USB flasher 
#### Software – Quartus prime
## Theory:
#### Adders are digital circuits that carry out addition of numbers.
#### Half Adder:
#### Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

#### Sum = A’B+AB’ =A ⊕ B Carry = AB

#### Full Adder:
#### Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

##### Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

## Procedure:
#### 1. Use module projname(input,output) to start the Verilog programmming.
#### 2. Assign inputs and outputs using the word input and output respectively.
#### 3. Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
#### 4. Use each output to represent one for Sum and the other for Carry.
#### 5. End the verilog program using keyword endmodule.
## Program:
#### Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
#### Developed by: SARAVANAN PARTHIBAN VIJAYALAKSHMI
#### RegisterNumber:  23002149

#### Half Adder:
```
module halfAdder (A,B,C,S);
input A,B;
output S,C;
xor (S,A,B);
and (C,A,B);
endmodule
```
#### Full Adder:
```
module fullAdder (A,B,Cin,S,Cout);
input A,B,Cin;
output S,Cout;
assign S = ((A^B)^Cin);
assign carry = ((A&B)|(B&Cin)|(Cin&A));
endmodule
```

## Output:

### Half Adder - 

#### RTL:
![image](https://github.com/SaravananPV3010/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139754526/ddfb15b9-a67b-45ab-868b-9bd7ea0a5ab1)

#### Truth Table:
![image](https://github.com/SaravananPV3010/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139754526/b39d299a-077e-4217-b595-480a941db23f)

#### WaveForm:
![image](https://github.com/SaravananPV3010/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139754526/03770ca8-be30-4f64-8b5a-58b2dcd4398d)


### Full Adder - 

#### RTL:
![image](https://github.com/SaravananPV3010/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139754526/605ab8af-dbc7-49d4-a178-0f6b3f010074)

#### Truth Table:
![image](https://github.com/SaravananPV3010/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139754526/4b49dc51-3457-4557-8c6d-250deddc076f)

#### WaveForm:
![image](https://github.com/SaravananPV3010/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139754526/63dd6044-4792-43c9-ab28-1f40abb587ab)


## Result:
#### Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
