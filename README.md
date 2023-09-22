# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

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

1. Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3.Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4. Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.

6. Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.

## Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: algu nachiyar k 
RegisterNumber:212222240006  

## Half Adder:
```
module exppp(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum= a^b;
assign carry = a&b;
endmodule
```
## Full Addder: 
```
module full(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum= a^b^cin;
assign carry = (a&b)|((a^b)&cin);
endmodule
```
## OUTPUT:
## Half Adder Truthtable:
![image](https://github.com/Nachiyarr/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/113497340/c55ba7c8-0d68-49f9-b573-374f226b84d1)

##  Half Adder RTL realization:
![exp 3 halfv addder](https://github.com/Nachiyarr/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/113497340/41e352a9-2924-49f6-8277-8a95ba703b94)



### Timing Diagram Half Adder:
![image](https://github.com/Nachiyarr/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/113497340/d6f4b0f3-47a0-4903-8ca1-8f5eeb777208)


## Full Adder Truthtable:
![image](https://github.com/Nachiyarr/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/113497340/0f4c4196-0e35-452d-8c15-fec3d34fcb30)


## Full Adder RTL realization:
![full](https://github.com/Nachiyarr/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/113497340/c76a3754-8193-4a88-ae69-3d7a6e0e1f4f)


## Timing Diagram Full Adder:

![image](https://github.com/Nachiyarr/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/113497340/3d128a5e-a2b8-447f-a190-61a011d1ed2d)








### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
