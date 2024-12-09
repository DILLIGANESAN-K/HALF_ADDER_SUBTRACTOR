# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
![IMG-20241209-WA0032](https://github.com/user-attachments/assets/9afca601-8f6d-470d-9a53-a433b3d8785a)
![IMG-20241209-WA0034](https://github.com/user-attachments/assets/ed5ce987-5e0b-448d-9819-b5cd1884cda6)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
Half Adder module hadd(a,b,sum,cout); 
input a,b; output sum,cout; 
xor g1(sum,a,b); and g2(cout,a,b); 
endmodule
Half Subtractor module hsub(a,b,sub,bout); 
input a,b; output sub,bout; wire w1; 
xor g1(sub,a,b); not g2(w1,a); and g3(bout,w1,b); 
endmodule

Developed by:Dilli ganesan 
RegisterNumber:24010195

**RTL Schematic**
Half Adder
![IMG-20241209-WA0033](https://github.com/user-attachments/assets/62dfc645-7ba8-40ca-b666-434473cec57e)
Half Subtractor
![IMG-20241209-WA0037](https://github.com/user-attachments/assets/dc386fdf-cc3e-4355-b5cd-263944546cad)

**Output/TIMING Waveform**
Half Adder
![IMG-20241209-WA0040](https://github.com/user-attachments/assets/11a0a7f5-35fc-4341-a172-b429e98133ce)
Half Subtractor
![IMG-20241209-WA0035](https://github.com/user-attachments/assets/39ce4fb0-157d-4ca1-8121-e293e1cfb7c2)

**Result:**
 Thus the half adder and half subtractor circuits were successfully designed, and
their truth tables were verified in Quartus using Verilog programming.
