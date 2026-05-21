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

<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/e544d079-c38f-4295-a6b4-37d3e9867479" />


FULL SUBTRACTOR:

<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/dc157db6-cedc-4035-8cef-f5d320297c14" />


**Procedure**
```
Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.
```

**Program:**

FULL ADDER:
```
module exp3de1(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule

```
FULL SUBTRACTOR:
```
module exp3de2(df, bo, a, b, bin);

    output df;
    output bo;

    input a;
    input b;
    input bin;

    wire w1, w2, w3;

    assign w1 = a ^ b;
    assign df = w1 ^ bin;

    assign w2 = (~a) & b;
    assign w3 = (~w1) & bin;

    assign bo = w2 | w3;

endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:SHALINI D
RegisterNumber:212225040398
*/

**RTL Schematic**
FULL ADDER:
<img width="1920" height="1080" alt="Screenshot 2026-05-21 135729" src="https://github.com/user-attachments/assets/30f8f538-1747-4084-9cf2-08107b60a8a2" />
FULL SUBTRACTOR:
<img width="1920" height="1080" alt="Screenshot 2026-05-21 143015" src="https://github.com/user-attachments/assets/8bea29f2-d170-4a91-9cb5-1a6f8894001e" />


**Output Timing Waveform**
FULL ADDER:
<img width="1920" height="1080" alt="Screenshot 2026-05-21 142209" src="https://github.com/user-attachments/assets/5d6792a2-f77e-478a-a9d8-095ceff0ea8b" />
FULL SUBTRACTOR:
<img width="1920" height="1080" alt="Screenshot 2026-05-21 144022" src="https://github.com/user-attachments/assets/cf3f1ed8-cea3-403b-bd1b-becedc7fe717" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



