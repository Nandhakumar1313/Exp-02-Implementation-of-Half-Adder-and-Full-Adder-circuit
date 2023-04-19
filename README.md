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
```
Developed by:  G.R.Nandhakumar
RegisterNumber:  212222100029

module ha(x,y,s,c);
input x,y;
output s,c;
xor(s,x,y);
and(c,x,y);
endmodule

module full_adder(x, y, z, s, c, x1, x2, x3);
input x,  y,z;
output s ,c, x1, x2, x3;
xor(x1, x, y);
xor(s, x1, z);
and(x2, x, y);
and(x3, x1, z);
or(c, x2, x3);
endmodule
``` 

### Output:
### RTL
![ha1](https://user-images.githubusercontent.com/120230694/232973866-792b8423-1090-43aa-938c-9efd21a041bf.png)
![fa1](https://user-images.githubusercontent.com/120230694/232973913-6ad4c61f-95e9-4a7b-afa1-846ac7cf3c24.png)

### TIMING DIAGRAM
![ha2](https://user-images.githubusercontent.com/120230694/232974261-770359d5-f82a-4e1d-8fa0-bd499a79eb12.png)
![fa2](https://user-images.githubusercontent.com/120230694/232974277-8ef8c5d2-e1ec-4d1b-ab83-a85774291c6c.png)


### TRUTH TABLE
![HATT](https://user-images.githubusercontent.com/120230694/232974001-fa1b8da2-6f84-40ff-85fb-5aede743b1ac.png)

![FATT](https://user-images.githubusercontent.com/120230694/232974057-2c138d98-5e3b-41a9-ab0a-24efd60dcb70.png)


### Result:
Therefore,half adder and full adder is verified
