<img width="1920" height="1017" alt="519614318-adda3638-f4d7-41d2-9468-2ec4bcd210fd" src="https://github.com/user-attachments/assets/b18f2fbd-1890-47c6-b5e6-b0cd95d42bc6" /><img width="1920" height="1017" alt="519614318-adda3638-f4d7-41d2-9468-2ec4bcd210fd" src="https://github.com/user-attachments/assets/c39f3f09-5e51-46f3-9c21-09ca2075c478" /># FULL_ADDER_SUBTRACTOR

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
FULL ADDER:
```
module exp4(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule
```
FULL SUBRACTOR:
```
module exp4(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule
```
 Developed by:AJAIRAJ J
 RegisterNumber:212225220004


**RTL Schematic**
FULL ADDER:
<img width="1920" height="1017" alt="519614318-adda3638-f4d7-41d2-9468-2ec4bcd210fd" src="https://github.com/user-attachments/assets/5e4d5340-ced3-479d-8eaa-bb66c8b8aaa3" />

FULL SUBRACTOR:

<img width="1920" height="1017" alt="519615730-d9b5d0b1-7302-45de-aac6-b4ee96a399d4" src="https://github.com/user-attachments/assets/6e23282b-2139-44a2-9739-02cc71e9fdb1" />



**Output Timing Waveform**
FULL ADDER:
<img width="1920" height="1017" alt="519614761-def6f871-2576-45d0-85fb-5e6484df5157" src="https://github.com/user-attachments/assets/b3261f0f-856e-454a-bd02-c494db63230e" />

FULL SUBRACTOR

<img width="1920" height="1017" alt="519614976-440968a7-a938-4e46-bbba-2c8cccdcbc52" src="https://github.com/user-attachments/assets/ab23aa6c-f905-4556-ae63-1a737104aa92" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



