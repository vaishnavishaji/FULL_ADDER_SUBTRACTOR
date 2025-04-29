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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Vaishnavi S.A RegisterNumber:212223220119
*/

Full Adder
```
module Experiment4a(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule
```
Full Subtractor
```
module Experiment4b(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule
```


**RTL Schematic**

Full Adder
![389176160-629d34d3-12d4-4949-8b58-580ad3f46a1b](https://github.com/user-attachments/assets/3a68052e-0648-4330-b5b9-f662252f4a55)

Full Subtractor
![389176189-43a7748e-fc92-4e57-bbc1-fbd653a722a6](https://github.com/user-attachments/assets/a837117c-1dda-4c4c-a04b-5de10cfbdb59)


**Output Timing Waveform**

Full Adder
![389176316-dfedd4e3-628f-416b-991a-344389261b7a](https://github.com/user-attachments/assets/60f28742-7fa6-49a3-b351-aa8ecf6b2464)

Full Subtractor
![389176332-74b42eea-3319-436a-a36c-55f8a06f1c5d](https://github.com/user-attachments/assets/d990fa95-b78f-4e17-bb96-9d6e83c510f9)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



