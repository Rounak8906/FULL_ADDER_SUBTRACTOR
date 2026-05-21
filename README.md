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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
### FULL ADDER
```
module full_adder(sum, carry, a, b, cin);
    output sum;
    output carry;
    input a;
    input b;
    input cin;

    assign sum = a ^ b ^ cin;
    assign carry = (a & b) | (cin & (a ^ b));
endmodule
```
### FULL SUBTRACTOR
```
module full_subtractor(diff, borrow, a, b, bin);
    output diff;
    output borrow;
    input a;
    input b;
    input bin;

    assign diff = a ^ b ^ bin;
    assign borrow = (a & b) | ((a ^ b) & bin);
endmodule
```
**RTL Schematic**
### FULL ADDER
<img width="928" height="333" alt="image" src="https://github.com/user-attachments/assets/952caf75-0fa5-46e2-8c49-47b659c93ca2" />

### FULL SUBTRACTOR
<img width="937" height="325" alt="image" src="https://github.com/user-attachments/assets/22950480-3657-4738-ba13-38a02aad7cb1" />

**Output Timing Waveform**
### FULL ADDER
<img width="1876" height="457" alt="Screenshot 2026-05-21 201254" src="https://github.com/user-attachments/assets/821f557c-0a41-468b-ab60-d0daeccb95ad" />

### FULL SUBTRACTOR

<img width="1583" height="382" alt="Screenshot 2026-05-21 202202" src="https://github.com/user-attachments/assets/8fc1d67b-ed72-4815-9f05-9d3b65cd532d" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



