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

Full Adder

![image](https://github.com/PranaveshSaikumar/FULL_ADDER_SUBTRACTOR/assets/151001393/9d270612-d92b-46d3-9474-2d0a351bf953)

Full Subtractor

![image](https://github.com/PranaveshSaikumar/FULL_ADDER_SUBTRACTOR/assets/151001393/e791588c-cec1-4f39-93ae-d1673580f667)


**Procedure**

**Full Adder:**
```
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
```

**Program:**

Register Name: THIRUMURUGAN R

Register No.: 212223220118

Full Adder
```
module fulladder(a,b,cin,sum,carry);
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
```
Full Subtractor
```
module fullsub(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
**RTL Schematic**

Full Adder

![full adder logic gate](https://github.com/PranaveshSaikumar/FULL_ADDER_SUBTRACTOR/assets/151001393/30274673-8b73-48dd-a07f-ea8825b0273f)

Full Subtractor

![Full sub logic gate](https://github.com/PranaveshSaikumar/FULL_ADDER_SUBTRACTOR/assets/151001393/9ab5cc38-b753-48c6-ada0-a41c1df85e5d)

**Output Timing Waveform**

Full Adder

![full adder waveform](https://github.com/PranaveshSaikumar/FULL_ADDER_SUBTRACTOR/assets/151001393/d78d447b-c0b5-49bb-8756-4d1b6f85d48c)

Full Subtractor

![full sub waveform](https://github.com/PranaveshSaikumar/FULL_ADDER_SUBTRACTOR/assets/151001393/10dddfb1-205e-48af-8729-71eb215ca2b2)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



