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
```
HALF ADDER
```
module halfadder(a,b,s,c);
module fulladd (a,b,sum,carry);
input a,b;
output sum,carry;
assign sum = (a^b);
assign carry = (a&b);
endmodule
```
## FULL ADDER
```
module fulladd (a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = (a^b^c);
assign carry = ((a&b)|(a^b)&c);
endmodule

``` 

### Output:

### RTL
## HALF ADDER
![239603036-0e997b08-8c46-4050-8d4f-78dfcdc494c7](https://github.com/Nandhakumar1313/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/120230694/0b7ce05b-c8a4-4c39-85e1-26aa2aa1b4dd)

## FULL ADDER
![239602892-96fa2eb7-593f-40f4-a1b6-ea639306c2f7](https://github.com/Nandhakumar1313/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/120230694/da45bed5-2077-4c5c-9e0f-6ebe4615bcc6)



### TIMING DIAGRAM
## HALF ADDER
![237398347-9b6a0cd5-2e1e-4fba-bb89-2cce99b784ba](https://github.com/Nandhakumar1313/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/120230694/4dff9560-d268-4e94-bf49-bc5ba31dc549)

## FULL ADDER
![237398516-9fde0ab9-1de6-4d66-b14b-70dd2d016a1b](https://github.com/Nandhakumar1313/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/120230694/aff5f564-f041-4ccb-8e15-b9b3b55f7ee6)


### TRUTH TABLE
## HALF ADDER
![HATT](https://user-images.githubusercontent.com/120230694/232974001-fa1b8da2-6f84-40ff-85fb-5aede743b1ac.png)

## FULL ADDER
![FATT](https://user-images.githubusercontent.com/120230694/232974057-2c138d98-5e3b-41a9-ab0a-24efd60dcb70.png)


### Result:
Therefore,half adder and full adder is verified
