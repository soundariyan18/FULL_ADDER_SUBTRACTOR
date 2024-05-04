# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
Developed by    : M.N.SOUNDARIYAN 
RegisterNumber  : 212222230146
```
```verilog
module FULL_addsub(a,b,Cin,sum,carry,BO,DIFF);
input a,b,Cin;
output sum,carry,BO,DIFF;
assign sum = a^b^Cin;
assign carry = (a&b)|(a&Cin)|(b&Cin);
assign DIFF = a^b^Cin;
assign BO = (~a & b)|(~(a^b)&Cin);
endmodule

```

**RTL Schematic**
![image](https://github.com/soundariyan18/FULL_ADDER_SUBTRACTOR/assets/119393307/b6341f08-9160-41fd-aeea-6a67fe254b2e)


**Output Timing Waveform**
**FULL ADDER**
![image](https://github.com/soundariyan18/FULL_ADDER_SUBTRACTOR/assets/119393307/5b1f42fa-1059-4fbb-b811-350cd5aa79c9)

**FULL SUBRACTOR
![image](https://github.com/soundariyan18/FULL_ADDER_SUBTRACTOR/assets/119393307/ce4ed557-2927-4a22-bfeb-4be3a4f2638f)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



