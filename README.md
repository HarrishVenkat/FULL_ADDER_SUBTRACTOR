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
```
## Full Adder:
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

## Full Subtractor: 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Harrish Venkat V
RegisterNumber: 212223240049
*/
```
module FULLADDERSUB(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule
```

**RTL Schematic**
![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/6fb0a11a-bfdb-481c-b5e9-fb875f3fda3d)

**Output Timing Waveform**
## Full_adder

![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/ed090da8-7d33-4f76-ab63-2b927df28e15)
## Full_subtractor


![image](https://github.com/HarrishVenkat/FULL_ADDER_SUBTRACTOR/assets/144979588/e9c6cee9-ea48-46d9-b33d-72e3414ad75d)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



