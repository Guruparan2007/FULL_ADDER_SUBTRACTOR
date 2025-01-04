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

FULL ADDER:

![Screenshot 2025-01-04 080556](https://github.com/user-attachments/assets/8dff87a8-81e2-4438-a9fd-4600bc9cc9b7)


FULL SUBRACTOR:

![Screenshot 2025-01-04 080634](https://github.com/user-attachments/assets/6bd06480-f279-4a82-9404-116367ba5cb6)






**Procedure**
~~~
FULL ADDER:

1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

FULL SUBRACTOR:


1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
~~~


**DEVELOPED BY**  GURUPARAN G  
**REFERENCE NO**  24001677


**Program:**


FULL ADDER:
~~~
module Lab4Fa (A, B, Cin, sum, car) ;
input A,B,Cin;
output sum, car;
assign sum = A ^ B ^ Cin;
assign car = ( (A & B) | ( (A ^ B) &Cin) ) ;
endmodule
~~~

FULL SUBRACTOR:
~~~
module Lab4Fs (A, B, Bin, diff, bor) ;
input A, B, Bin;
output diff, bor;
assign diff = A ^ B ^ Bin;
assign bor = ((A & B) | ( (A ^ B) & Bin) ) ;
endmodule
~~~


**RTL Schematic**

FULL ADDER:

![Screenshot 2025-01-04 080756](https://github.com/user-attachments/assets/f6d787e9-0b6c-459c-9d03-f537372fd38b)

FULL SUBRACTOR:

![Screenshot 2025-01-04 080809](https://github.com/user-attachments/assets/9b8733ae-e4eb-4e98-9852-5ddb8204f944)

**OUTPUT TIMING WAVEDIAGRAM**

FULL ADDER:


![Screenshot 2025-01-04 080850](https://github.com/user-attachments/assets/7127961c-2ac3-4b8f-afac-3f24d92c3003)



FULL SUBRACTOR:



![Screenshot 2025-01-04 080914](https://github.com/user-attachments/assets/dcb4c6f1-6cd6-4daf-827b-2e4ee6974e63)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



