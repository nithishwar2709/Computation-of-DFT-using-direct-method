# EXPT 1: Computation-of-DFT-using-direct-method

# AIM: 
  To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
## DISCRETE FOURIER TRANSFORM:

```
clc; 
clear; 
xn=[1 2 3 4 4 3 2 1]; 
 
n1=0:1:length(xn)-1; 
subplot(3,1,1); 
plot2d3(n1,xn); 

xlabel('Time n'); 
ylabel('Amplitude xn'); 
title('Input Sequence'); 

j=sqrt(-1); 
N=length(xn); 
Xk=zeros(1,N); 
for k=0:N-1 
for n=0:N-1 
Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N); 
end 
end 
disp(Xk) 
K1=0:1:length(Xk)-1; 
magnitude=abs(Xk) 
subplot(3,1,2); 
plot2d3(K1,magnitude); 

xlabel('frequency(Hz)'); 
ylabel('magnitude(gain)'); 
title('magnitude spectrum'); 

angle = atan(imag(Xk),real(Xk)) 
subplot(3,1,3); 
plot2d3(K1,angle); 

xlabel('frequency(Hz)'); 
ylabel('Phase'); 
title('Phase spectrum'); 

```

### CALCULATIONS: 


![20260224_204739](https://github.com/user-attachments/assets/3cf22a7e-ade6-451b-a1c6-2199adf994d8)
![20260224_204743](https://github.com/user-attachments/assets/99bce737-d484-47d3-b76c-20e95e022b60)
![20260224_204747](https://github.com/user-attachments/assets/02ff5b17-74ee-4388-a6da-85fd69f378e7)

### SAMPLE OUTPUT: 

<img width="1916" height="1190" alt="Screenshot 2026-02-23 093317" src="https://github.com/user-attachments/assets/1b4691aa-ee5c-4637-aed5-e1a41ae6d698" />

# RESULT: 

Thus, DFT using direct method for two given sequences were performed and its result was verified.


