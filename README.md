### EXPT 2a: LINEAR CONVOLUTION-USING-DFT
### AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

### APPARATUS REQUIRED
PC installed with SCILAB

### PROGRAM:
LINEAR CONVOLUTION
```
clc;
clear;
x = [1 2 3 4];
h = [2 4 8 6];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
conv_sum = 0;
for j = 1:i
if (((i-j+1) <= n)&(j <=m))
conv_sum = conv_sum + x(j)*h(i-j+1);
end;
y(i) = conv_sum;
end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
```





### CALCULATIONS:

<img width="970" height="1599" alt="WhatsApp Image 2026-11-10 at 5 33 41 PM" src="https://github.com/user-attachments/assets/034bf7dc-35ff-465a-bbe7-f82b9619d59f" />

<img width="985" height="1600" alt="WhatsApp Image 2026-11-10 at 5 34 30 PM" src="https://github.com/user-attachments/assets/d6298d46-e20b-4430-bace-d56db9266b5e" />

<img width="1600" height="315" alt="WhatsApp Image 2026-11-10 at 5 34 48 PM" src="https://github.com/user-attachments/assets/9aa42421-efc9-49ea-8f50-901fd31b2d50" />

### SAMPLE OUTPUT:


<img width="1600" height="1118" alt="image" src="https://github.com/user-attachments/assets/61557288-6388-4ebe-892c-8a138a08c7f8" />



### RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
