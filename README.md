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
module fulladd1(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor g1(sum,a,b,c);
assign carry=((a&b)|(b&c)|(c&a));
endmodule 
module fullsub1(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
xor g1(diff,a,b,c);
assign borrow=((~a&c)|(~a&b)|(b&c));
endmodule 

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Akshaya Sree G RegisterNumber:25018408
*/

**RTL Schematic**
<img width="1920" height="1020" alt="Screenshot 2025-11-17 131516" src="https://github.com/user-attachments/assets/5aceaac6-e932-49f6-8036-abb0bf94d3d8" />
![WhatsApp Image 2025-11-17 at 13 40 48_0dd7ce0f](https://github.com/user-attachments/assets/3f4d11b6-6d62-4744-8def-c2e9580265be)



**Output Timing Waveform**
<img width="1920" height="1020" alt="Screenshot 2025-11-17 131953" src="https://github.com/user-attachments/assets/bef480d1-ec5e-4a63-ad2b-e6ea7fb5f04a" />
<img width="1920" height="1020" alt="Screenshot 2025-11-17 134035" src="https://github.com/user-attachments/assets/6336cea7-f13e-42e8-a95c-20e52c35efea" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



