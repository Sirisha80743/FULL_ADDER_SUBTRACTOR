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
**Figure -1 FULL ADDER**

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Full Adder Truth Table**

![full adder](https://github.com/user-attachments/assets/c61c3bd3-ba6a-4159-8df8-f927d1de99c5)


**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Full Subtractor Truth table**

![full subtractor](https://github.com/user-attachments/assets/fabb9d22-fa3d-4644-bfdb-9700c484aaf4)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: P Sirisha RegisterNumber:24002102
*/

Full Adder
```
module fa(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum=(A^B^Cin);
assign carry=(A&B)|((A^B)&Cin);
endmodule
```
Full Subtractor
```
module fs(A,B,Bin,diff,borr);
input A,B,Bin;
output diff,borr;
assign diff=(A^B^Bin);
assign borr=((~A&B)|(~(A^B)&Bin));
endmodule
```
**RTL Schematic**

 Full Adder
![ex 4a](https://github.com/user-attachments/assets/cb897670-f0ed-4212-8b74-f3da8e3694e4)

Full Subtractor
![ex 4b](https://github.com/user-attachments/assets/53717d51-5090-4f85-8dd7-8a303c00c6f1)

**Output Timing Waveform**

 Full Adder
![ex 4a wave](https://github.com/user-attachments/assets/9391309d-bb01-42b3-a953-e0a9b50ae4f3)

Full Subtractor
![ex 4b wave](https://github.com/user-attachments/assets/63dc7281-280a-48ef-ae1f-f51d1595337e)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



