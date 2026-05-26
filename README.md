# MEAN-VARIANCE-CROSS_CORRELATION-USING-SCILAB
AIM: To write a program for mean, variance and cross correlation in SCILAB and verify the output.

EQUIPMENTS Needed

· Computer with i3 Processor

· SCI LAB

Algorithm

Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.

Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.

Evaluate the Function: Compute the function values at each of these sample points.

Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.

Display Results: Output the computed mean variance and Cross Correlation

PROCEDURE

· Refer Algorithms and write code for the experiment.

· Open SCILAB in System

· Type your code in New Editor

· Save the file

· Execute the code

· If any Error, correct it in code and execute again

· Verify the generated results

PROGRAM
```
clear;
clc;
clear;
function X=f(x)
    z=3*(2-x)^2
    X=x*z
endfunction
a=0;
b=1;
EX=intg(a,b,f);
function Y=c(y)
    z=3*(2-y)^2
    Y=y*z
endfunction
EY=intg(a,b,c);
disp(EX,"i)Mean of X=")
disp(EY,"Mean of Y=")

function X=g(x)
    z=3*(2-x)^2
    X=x^2*z
endfunction
a=0;
b=1;
EX2=intg(a,b,g);
function Y=h(y)
    z=3*(2-y)^2
    Y=y^2*z
endfunction
EY2=intg(a,b,h);
vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;
disp(vX2,"ii) Variance of X");
disp(vY2,"Variance of Y");

x=[1 3 4 5 9 2 3 8];
y=[2 5 8 4 7 1 3 7];
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```
OUTPUT:

<img width="1918" height="1197" alt="image" src="https://github.com/user-attachments/assets/7cc85f08-252a-47b0-8cfd-6c20870a2747" />

Cross Correlation

Type in the reference sequence = [1 3 4 5 9 2 3 8]

Type in the second sequence = [2 5 8 4 7 1 3 7]



calculation:

<img width="884" height="1398" alt="image" src="https://github.com/user-attachments/assets/12d4fc81-bfb6-40a4-a0aa-6c80e8ef7df9" />
<img width="916" height="1424" alt="image" src="https://github.com/user-attachments/assets/2f4c11c0-0fc3-4cd6-ab5d-2ecc1544fba3" />
<img width="1600" height="1082" alt="image" src="https://github.com/user-attachments/assets/b3226adf-51ab-4051-8fd9-628ebee35ec6" />



RESULT:

Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
