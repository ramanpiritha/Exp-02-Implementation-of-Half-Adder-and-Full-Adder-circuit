# Name: Piritharaman R
# Ref No: 23013537


# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using verilog programming

HALF-ADDER:

module exp3(sum, carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

FULL-ADDER:

module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule

TRUTH TABLE:

HALF-ADDER:
![image](https://github.com/ramanpiritha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147084116/b31b04a0-5ee9-4eda-8a26-6f457bc493ae)

FULL-ADDER:
![image](https://github.com/ramanpiritha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147084116/bcbd9c96-de7b-4d15-bbd5-a575be23fd15)


### RTL REALIZATION:
HALF-ADDER:
![image](https://github.com/ramanpiritha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147084116/4a9ce3fe-f742-4458-939c-eb15800d946c)

FULL-ADDER:
![image](https://github.com/ramanpiritha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147084116/9404c48a-666d-49f8-8ffe-29ab6a9b9043)


## OUTPUT:
HALF-ADDER:
![image](https://github.com/ramanpiritha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147084116/4e037751-908a-42d1-88f5-26f6aef775ef)

FULL-ADDER:
![image](https://github.com/ramanpiritha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147084116/8c2fc4d1-913b-4e61-93ae-2b59fb1a432e)



### Result:
Thus the given logic functions are implemented using and their operations are verified using verilog using verilog programming.
