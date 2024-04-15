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
FULL ADDER:
![Screenshot 2024-04-15 175019](https://github.com/ZafreenJagir/FULL_ADDER_SUBTRACTOR/assets/144870573/55e7b246-2834-4f1d-8650-651320aaa2b9)


FULL SUBTRACTOR:
 ![Screenshot 2024-04-15 175052](https://github.com/ZafreenJagir/FULL_ADDER_SUBTRACTOR/assets/144870573/29a4e873-fc6b-45e1-aa0e-24eddf892146)


**Procedure**

Write the detailed procedure here
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

## PROGRAM
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Zafreen J
RegisterNumber:212223040252
module FULL_addsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum = a^b^cin;
assign carry = (a&b) | (b&cin) | (a&cin);
wire a0;
not (a0,a);
//Write syntax for full subtractor Borrow and Difference in data flow modelling
assign DIFF = a^b^cin;
assign BO = (a0&b) | (b&cin) | (a0&cin);
endmodule
*/
```


**RTL Schematic**

![Screenshot 2024-04-15 175325](https://github.com/ZafreenJagir/FULL_ADDER_SUBTRACTOR/assets/144870573/0b5fbabc-7118-4fa9-a82b-bdc1b4f9bdc3)


**Output Timing Waveform**

![Screenshot 2024-04-15 175411](https://github.com/ZafreenJagir/FULL_ADDER_SUBTRACTOR/assets/144870573/c58aab8e-370f-432e-beb2-30ea5ea35911)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



