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
module FULLADD(a,b,cin,sum,carry);
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
~~~


full subtractor
~~~
module FULLSUB(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
~~~


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Yugabharathi.T RegisterNumber:24900006
*/

**RTL Schematic**

full adder

![394196174-2335a954-28a1-4074-94e0-4c0731fbe4da](https://github.com/user-attachments/assets/abfb35e7-b894-460e-a2bf-5670ba3c686e)

full subtractor

![383135147-a699cfeb-efb4-4280-b1fe-cf0debf77873](https://github.com/user-attachments/assets/11d317bd-b6e8-495d-8ed0-2eeffd5287ce)

**Output Timing Waveform**

full adder

![392022688-7599b53b-42de-4be3-b2ad-0544f796c2f2](https://github.com/user-attachments/assets/63492276-457e-41f6-a5d7-9562bc0e5a1b)

full subtractor

![392022832-b42f9eb9-b7c0-463d-a9f6-7a187a420e83](https://github.com/user-attachments/assets/d37dc4cb-56e9-4e2c-b24a-4d5913a90f35)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



