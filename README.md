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
FULLADDER
![FA TRUTH TABLE](https://github.com/user-attachments/assets/70f7cfa8-8365-4288-bb17-05b9d65c29f2)

FULL SUBTRACTOR:
![FS TT](https://github.com/user-attachments/assets/153ddaeb-3e07-40dc-b84f-2b2a1c6bf546)

**Procedure**
```
1. Open Quartus Software   
2. Create a New Project  
3. Create a New Design File  
4. Compile the Program  
5. Generate RTL Schematic  
6. Create Nodes for Inputs/Outputs  
7. Generate Timing Diagram  
8. Simulate Different Input Combinations  
9. Save Your Work  
```

**Program:**
```
Name :Prasana v
Register no:212223040150
```
```
#Full adder
module proj_41(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

#Full Subtractor
module proj_42(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule

```

**RTL Schematic**

#FULL ADDER
![FA RTL](https://github.com/user-attachments/assets/bed46df2-925a-4c49-8327-96f16d3bb4a3)
#FULL SUBTRACTOR
![FS RTL](https://github.com/user-attachments/assets/e939939e-7400-4c05-b3a5-5ff75df446b6)

**Output Timing Waveform**
#FULL ADDER
![FA](https://github.com/user-attachments/assets/75e15a41-8be5-480a-a67a-691818276145)
#Full Subtractor
![FS](https://github.com/user-attachments/assets/63813acc-0a94-42a9-a683-7644f433734c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



