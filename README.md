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
FULL ADDER

![398612828-62b8ca6a-67b3-475f-8bc8-831acae86172](https://github.com/user-attachments/assets/c2fc296a-e3c4-400e-915a-11fca78526bf)

FULL SUBTRACTOR

![398612851-ffe9d0fb-6729-4553-b3ea-ab1951b2bbdf](https://github.com/user-attachments/assets/0f58e346-c30a-472e-8642-3322f730a2b4)

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.*/ 
Developed by:NIRANJAN S
RegisterNumber:24900209
~~~
i)FULL ADDER
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
~~~
~~~
ii)FULL SUBTRACTOR
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
~~~

**RTL Schematic**
FULL ADDER
![398612429-815e9ef7-9ad6-4573-9d0e-e0c45545419f](https://github.com/user-attachments/assets/cbc4845d-6148-438d-b3eb-dfcb45ed7768)
FULL SUBTRACTOR
![398612464-e89bb1fa-a5a8-42f5-af72-03fa362c2a00](https://github.com/user-attachments/assets/5502d8cf-cebc-4b3b-ae9b-9fe4aff505e6)

**Output Timing Waveform**
FULL ADDER
![398612556-444b5c95-a8e3-4dbc-bf2b-cbbb19e04ff8](https://github.com/user-attachments/assets/f81c7379-151e-45d5-8317-8b1357af2049)
FULL SUBTRACTOR
![398612568-3c2d0071-45cc-44b9-9a65-aa9236be44a5](https://github.com/user-attachments/assets/11a5f2ab-4328-43f6-ab5f-5828f14a0215)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



