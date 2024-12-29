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

Full adder

![392022409-4f221821-70bf-42e5-a2fc-654c0e2dd2d1](https://github.com/user-attachments/assets/59aa2cf2-f69c-4382-98db-bb557134360e)

Full subtractor

![392022551-ff1bf36f-7f03-4d61-ba9c-d1fe80c26f1e](https://github.com/user-attachments/assets/337ef52d-6030-4c4a-b33e-5b7abb7a8b2c)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**
full adder
~~~
module exp4a(sum,cout,a,b,cin); 
output sum; 
output cout; 
input a,b,cin;
wire s1,c1,c2;
xor(s1,a,b); 
and(c1,a,b); 
xor(sum,s1,cin); 
and(c2,s1,cin); 
or(cout,c2,c2); 
endmodule 
~~~


full subtractor
~~~
module exp4b(df,bo,a,b,bin); 
output df,bo; 
input a,b,bin; 
wire w1,w2,w3; 
assign w1=a^b; 
assign w2=(~a&b); 
assign w3=(~w1&bin); 
assign df=w1^bin; 
assign bo=w2|w3; 
endmodule
~~~


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Yugabharathi.T RegisterNumber:24900006
*/

**RTL Schematic**

full adder

![Screenshot 2024-12-29 174716](https://github.com/user-attachments/assets/ae7107a0-bcb3-4c18-8b19-80e2a7e3334f)

full subtractor

![Screenshot 2024-12-29 174726](https://github.com/user-attachments/assets/aa84a3ac-d1cd-4abb-8b60-fddc86f2d8c6)

**Output Timing Waveform**

full adder

![Screenshot 2024-12-29 174821](https://github.com/user-attachments/assets/da065c86-2e73-4d79-91f6-d40929ecd8ef)

full subtractor

![Screenshot 2024-12-29 174841](https://github.com/user-attachments/assets/3b9afa7c-3bdf-4c25-ae21-4dde3997354f)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



