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

## Truthtable
## Full_adder
![Screenshot 2024-03-18 181619](https://github.com/23005672/FULL_ADDER_SUBTRACTOR/assets/138971519/0b18ce6a-ab4d-42f7-aff3-e6422eb679df)
## Full_subtractor
![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/e4093225-ae2c-4f85-a3bc-c5d3ed5e439c)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Harrish Venkat V
RegisterNumber: 212223240049
*/
## Full_adder
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule

## Full_subtractor
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
**RTL Schematic**
![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/69a95518-9c12-436c-a17b-fab1244e12c1)

**Output Timing Waveform**
## Full_adder

![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/98202547-9ad0-4ef8-be27-06979f3993a6)
## Full_subtractor


![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/b2275adf-1eab-459e-85b8-47878b14f87b)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



