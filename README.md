# FULL_ADDER_SUBTRACTOR
DATE:10.12.2025

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
<img width="1280" height="965" alt="image" src="https://github.com/user-attachments/assets/00dce7d9-03f6-414e-85f7-9e03317f7e85" />

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

module DE4(A, B, C, S1, C1, D1, B1);
input A, B, C;       
output S1, C1, D1, B1;
assign S1 = A ^ B ^ C;                
assign C1 = A & B | A & C | B & C;    
assign D1 = A ^ B ^ C;                
assign B1 = (~A & (B | C)) | (B & C); 
endmodule


**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/b7a5bd3d-6ea9-4a52-8afd-301c21f009b6" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/b3a67779-db5f-4c36-b3e9-f802f50c20ad" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



