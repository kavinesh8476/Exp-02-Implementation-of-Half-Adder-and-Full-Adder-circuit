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
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Kavinesh M
RegisterNumber: 212222230064 
*/
### HALF ADDER
```
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### FULL ADDER
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
Logic symbol & Truthtable
RTL realization

### Output:
### RTL
### HALF ADDER
![image](https://user-images.githubusercontent.com/118466561/231657796-13a763a8-ed36-40aa-b079-03bd6fdf225b.png)

### FULL ADDER
![image](https://user-images.githubusercontent.com/118466561/231657759-fa43c64e-31e0-47f0-b083-2c7a1fd6961c.png)

### TIMING DIAGRAM
### HALF ADDER
![image](https://user-images.githubusercontent.com/118466561/231657881-8e6cdf57-aa23-4246-b74b-7a6f9917466f.png)

### FULL ADDER
![image](https://user-images.githubusercontent.com/118466561/231657905-4c96297a-1e9a-4511-afc4-844b9753e74a.png)

### TRUTH TABLE 
### HALF ADDER
![image](https://user-images.githubusercontent.com/118466561/231657998-351a49ba-a3d8-4cfb-aad6-d3ccf7789b19.png)

### FULL ADDER
![image](https://user-images.githubusercontent.com/118466561/231658688-a9a67ead-9be0-4b6e-860b-7680f4b8b05d.png)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
