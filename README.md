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

![hs-tt](https://github.com/user-attachments/assets/a109dd0c-4c1c-40d4-8734-62ef2d96cf1d)

![ha-tt](https://github.com/user-attachments/assets/b6eeb785-6680-4a53-8aca-7bbcded1d5f9)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: NANDA KISHOR S P
RegisterNumber: 24011485


//HALF ADDER

module ha_dataflow(a, b, s, ca);
 input a;
 input b;
 output s;
 output ca;
assign#2 s=a^b;
assign#2 ca=a&b;
endmodule

![ha-code](https://github.com/user-attachments/assets/2c24d424-febc-48a1-aaed-9b6153e4e066)


//HALF SUBRACTOR

module hs_dataflow(a, b, dif, bor);
 input a;
 input b;
 output dif;
 output bor;
wire abar;
assign#3 abar=~a;
assign#3 dif=a^b;
assign#3 bor=b&abar;
endmodule

![hs-code](https://github.com/user-attachments/assets/12ce4412-bcd3-48a9-ae0c-b424318cbaa7)



*/

**RTL Schematic**

//HALF ADDER

![ha-lg](https://github.com/user-attachments/assets/22ac2d17-d27a-4c9c-9332-6b8e77abb420)

//HALF SUBRACTOR

![hs-lg](https://github.com/user-attachments/assets/4a995539-581d-4562-8226-23221a493098)



**Output/TIMING Waveform**

//HALF ADDER

![ha-wf](https://github.com/user-attachments/assets/fec8325e-e03a-4fe8-8e2b-db66f2a01753)

//HALF SUBRACTOR

![hs-wf](https://github.com/user-attachments/assets/ab002d4f-4a74-4b9e-af22-0c198c9cd048)



**Result:**
