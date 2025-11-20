# FULL_ADDER_SUBTRACTOR
DATE:20.11.2025

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

<img width="364" height="288" alt="image" src="https://github.com/user-attachments/assets/779175a2-3f60-4112-9dc8-17f3ab3e96bd" />

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

module ex3 (a,b,c,x,y,z,sum,dif,car,bor);

input a,b,c,x,y,z;

output sum,dif,car,bor;

assign sum = a^b^c;

assign car = a&b | a&c | b&c;

assign dif = x^y^z;

assign bor = ~x&z | ~x&y | y&z;

endmodule

**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot (75)" src="https://github.com/user-attachments/assets/6cee69f4-66fa-4afd-89eb-c0c1ee35909c" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/5ba18607-930c-487c-a60a-3888979b3bbc" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



