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


FULL SUBRTACTOR:

![Screenshot 2025-01-04 080634](https://github.com/user-attachments/assets/6bd06480-f279-4a82-9404-116367ba5cb6)






**Procedure**
~~~
FULL ADDER:

1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

FULL SUBRTACTOR:


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


module full_add(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=(a^b^cin);
assign carry=((a&b)|((a^b)&cin));
endmodule
~~~

FULL SUBTRACTOR:
~~~


module full_sub(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=((a&b)|((a^b)&bin));
assign borr=((~a&b)|(b&bin)|(~a&bin));
endmodule
~~~


**RTL Schematic**

FULL ADDER:

![Screenshot 2025-01-04 093137](https://github.com/user-attachments/assets/0538513f-4f54-4437-aafc-85bedf91b437)


FULL SUBTRACTOR:


![Screenshot 2025-01-04 100444](https://github.com/user-attachments/assets/5c7a38e7-755b-4cae-9b8b-41be97280e38)



**OUTPUT TIMING WAVEDIAGRAM**

FULL ADDER:



![Screenshot 2025-01-04 093217](https://github.com/user-attachments/assets/f820488b-86db-4ee3-b46d-88c28adbbcc2)



FULL SUBTRACTOR:


![Screenshot 2025-01-04 093242](https://github.com/user-attachments/assets/2c0cd77f-2234-4be3-91df-463579d6d0c4)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



