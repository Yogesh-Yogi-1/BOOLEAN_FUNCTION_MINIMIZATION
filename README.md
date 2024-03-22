# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
Developed by: V.Yogesh
RegisterNumber:212223230250
*/
module booleanfunction(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
//type code for f2 as like f1
endmodule
```
**RTL realization**

**Output:**
![Screenshot 2024-03-15 144306](https://github.com/Yogesh-Yogi-1/BOOLEAN_FUNCTION_MINIMIZATION/assets/148514598/9d13590c-4773-4de1-b8a0-a78ce0522399)

**RTL**

**Timing Diagram**
![image](https://github.com/Yogesh-Yogi-1/BOOLEAN_FUNCTION_MINIMIZATION/assets/148514598/b695797e-8f4c-49ec-9260-8a50558b3f92)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

