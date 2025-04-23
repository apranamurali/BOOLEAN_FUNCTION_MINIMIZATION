BOOLEAN_FUNCTION_MINIMIZATION
AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F2=xy’z+x’y’z+w’xy+wx’y+wxy

Equipment Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

Theory

A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.

Procedure

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

Program:

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by : APARNA.M
RegisterNumber: 212223220008

*/
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1

module EX_02(a,b,c,d,w,x,y,z,f1,f2);
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

wire ybar,M,N,O;
not(ybar,y);
and(M,w,y);
and(N,x,y);
and(O,z,ybar);
or(f2,M,N,O);
endmodule
Output: image

Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

About
No description, website, or topics provided.
Resources
 Readme
License
 GPL-3.0 license
 Activity
Stars
 0 stars
Watchers
 0 watching
Forks
 1 fork
Report repository
Releases
No releases published
Packages
No packages published
Languages
VHDL
51.8%
 
Verilog
19.1%
 
Stata
13.6%
 
HTML
13.1%
 
Standard ML
2.4%
Footer
