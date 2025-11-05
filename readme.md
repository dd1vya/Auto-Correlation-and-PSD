## SIMULATION OF AUTOCORRELATION AND PSD USING SCILAB

### AIM:
Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

### EQUIPMENTS Needed
 Computer with i3 Processor  
 SCI LAB

### THEORY:
The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the
Fourier transform of the corresponding autocorrelation function.
<img width="998" height="198" alt="image" src="https://github.com/user-attachments/assets/81b01580-89ac-44e6-b6cf-5b9cc41164ec" />


### Algorithm
1. Load or Define the Signal: Input your time-domain signal.
2. Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3. Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like
Welch’s periodogram or by using the Fourier transform of the autocorrelation.
4. Plot Results: Visualize the autocorrelation function and PSD.

### PROCEDURE
 Refer Algorithms and write code for the experiment.  
 Open SCILAB in System  
 Type your code in New Editor  
 Save the file  
 Execute the code  
 If anyError, correct it in code and execute again  
 Verify the generated waveform using Tabulation and Model Waveform

### PROGRAM:
```
clc
clear all;
t=0:0.01:2*pi;
x=sin(2*t);
subplot(3,2,1);
plot(x);
au=xcorr(x,x);
Subplot (3,2,2);
plot (au);
v=fft(au);
subplot(3,2,3);
plot(abs(v));
fw=fft(x);
subplot(3,2,4);
plot(fw);
fw2=(abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```

### OUTPUT:
<img width="1779" height="965" alt="image" src="https://github.com/user-attachments/assets/261bf1e6-96ca-4d9d-aa30-12ce3fad9a3d" />


### RESULT:
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
