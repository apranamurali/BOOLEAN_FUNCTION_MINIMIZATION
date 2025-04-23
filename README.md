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

~~~
module booleanfn(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~b & ~d)|(~a & b & d)|(a & b & ~c));
endmodule
~~~

~~~
module booleanfnb(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((~y & z)|(w & y)|(x & y));
endmodule
~~~

Developed by: APARNA.M
RegisterNumber: 212223220008


**RTL realization**
f1
![Screenshot (196)](https://github.com/user-attachments/assets/81755bfe-362f-4aba-8b2a-f84f37d1d6a2)

f2
![Screenshot (198)](https://github.com/user-attachments/assets/ec0315e2-efdf-457a-a35c-0b4260cb614a)


**Output:**
![Screenshot (197)](https://github.com/user-attachments/assets/8778d584-0dba-4ca7-9b2c-aea173f39f3f)

![Screenshot (199)](https://github.com/user-attachments/assets/cdf57f18-2d2b-41aa-b8e5-ce9bc7dfbff4)




**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

