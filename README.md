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
## truthtable full adder:
![image](https://github.com/Priyangarajapandiyan/FULL_ADDER_SUBTRACTOR/assets/144872535/a39d205c-13df-4e00-9017-60f07902d2c1)
## full subractor:
![image](https://github.com/Priyangarajapandiyan/FULL_ADDER_SUBTRACTOR/assets/144872535/c70d8be5-2823-43be-953f-92286c4271b7)

**Procedure**
1)Create a New Project: *Open Quartus and create a new project by selecting "File" > "New Project Wizard." *Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA). 2)Create a New Design File: *Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." *Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language. 3)Write the Combinational Logic Code: *Open the newly created Verilog or VHDL file and write the code for your combinational logic. 4)Compile the Project: *To compile the project, click on "Processing" > "Start Compilation" in the menu. *Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device. 5)Analyze and Fix Errors: *If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. *Review and fix any issues in your code if necessary. *View the RTL diagram. 6)Verification: *Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF". *Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. *Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:THIRUMURUGAN R RegisterNumber: 212223220118
*/
## full adder
```
 module exp4(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule
```
 ## full subractor:
 ```
module exp4(diff,carry,a,b,c);
 input a,b,c;
 output diff,carry;
 xor(diff,a,b,c);
 assign carry= (~a)&c | (~a)&b | (b&c);
 endmodule
```
**RTL Schematic**
## RTL Schematic Full Adder:
![image](https://github.com/Priyangarajapandiyan/FULL_ADDER_SUBTRACTOR/assets/144872535/8a59b678-9efc-4f28-9ee8-4dd095456682)
## full subractor :
![image](https://github.com/Priyangarajapandiyan/FULL_ADDER_SUBTRACTOR/assets/144872535/6a7f24b8-dfb7-409f-bfa2-60ea6e5c4680)

**Output Timing Waveform**
## full adder:
![image](https://github.com/Priyangarajapandiyan/FULL_ADDER_SUBTRACTOR/assets/144872535/1f78e949-8648-4e5d-8e3c-e6a0faddb5a9)
## full subractor:
![image](https://github.com/Priyangarajapandiyan/FULL_ADDER_SUBTRACTOR/assets/144872535/653d882b-e645-4aa6-b6b4-a791e7101582)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



