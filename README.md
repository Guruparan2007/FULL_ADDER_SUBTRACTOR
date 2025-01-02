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


![Screenshot 2025-01-02 081759](https://github.com/user-attachments/assets/01a0d591-d612-47d7-92ed-0c1fc9cdeb9f)


FULL SUBRACTOR:


![Screenshot 2025-01-02 081822](https://github.com/user-attachments/assets/62ba2168-8fb2-45dc-8947-b0970b4416f2)





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
~~~
FULL ADDER :

module fulladd_top(a,b,cin,sum,carry);
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


FULL SUBRACTOR:


module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
~~~


**RTL Schematic**

FULL ADDER:

![Screenshot 2025-01-02 083208](https://github.com/user-attachments/assets/a10bac38-1e23-43ce-bf73-98f392f572e5)


FULL SUBRACTOR:

![Screenshot 2025-01-02 083523](https://github.com/user-attachments/assets/e0ceeeab-aa9e-41c3-b8b9-f72916de4e3b)

**OUTPUT TIMING WAVEDIAGRAM**

FULL ADDER:


![Screenshot 2025-01-02 081936](https://github.com/user-attachments/assets/4413b942-4a4f-46b5-94ed-72bd40089a99)


FULL SUBRACTOR:


![Screenshot 2025-01-02 082007](https://github.com/user-attachments/assets/b9542815-d1fa-43d4-979b-9d9f066d79d6)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



