DATE:22|10|24

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

![Screenshot 2024-12-25 144719](https://github.com/user-attachments/assets/ce68d997-1fbc-474b-bb0c-6366dca19930)

![Screenshot 2024-12-25 144743](https://github.com/user-attachments/assets/3c902779-3a8b-44d6-9874-9370ebc9d33e)

**Procedure**
1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.


**DEVELOPED BY** GURUPARAN G  **REFERENCE NO**24001677
**Program:**

![Screenshot 2024-12-25 144319](https://github.com/user-attachments/assets/4b22f4fb-11b7-4261-9622-020116ee168d)


![Screenshot 2024-12-25 144341](https://github.com/user-attachments/assets/de95a240-e90f-4e18-81a3-3b0ffad45df1)


**RTL Schematic**

![Screenshot 2024-12-25 144406](https://github.com/user-attachments/assets/ee2f840f-88d4-4fa0-b061-612a0446e6b9)

![Screenshot 2024-12-25 144431](https://github.com/user-attachments/assets/1b514857-0ce9-47c0-b26e-8a26285abeeb)

**Output TIMING WAVEDIAGRAM**

![Screenshot 2024-12-25 144506](https://github.com/user-attachments/assets/879c1226-09a6-41f9-82b9-b909cffc878f)


![Screenshot 2024-12-25 144539](https://github.com/user-attachments/assets/26e1cb0c-d984-4862-8e1b-535102615ce0)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



