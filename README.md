# FIR-FILTER-DESIGN
# EXP 4 e: Design-of-FIR-Digital-Filter-using-Bartlett-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Bartlett-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) = Wc/ %pi ; 
else 
hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Bartlett Window 
for n = 1:M 
W(n)=1-((2*abs((n-1)-((M-1)/2))/(M-1)); 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR LPF using Bartlett Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR LPF using Bartlett Window'); 
```
# CALCULATION:
![Bartlett manu](https://github.com/user-attachments/assets/9d53ad06-084a-41f9-a6b7-59650efac284)

# OUTPUT:
<img width="454" height="440" alt="LPF-Bartlett calculation" src="https://github.com/user-attachments/assets/8691f404-3620-47f6-9fad-68e09119e6cd" />
<img width="767" height="721" alt="LPF-Bartlett graph" src="https://github.com/user-attachments/assets/f6bef35c-1567-4bec-94d2-428b35e52c4d" />

# RESULT: 

Thus design of low pass FIR digital filter using-Bartlett-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) = 1-Wc/ %pi ; 
else 
hd(n) = -sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Bartlett Window 
for n = 1:M 
W(n)=1-((2*abs((n-1)-((M-1)/2)))/(M-1));  
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR HPF using Bartlett Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR HPF using Bartlett Window'); 
```
# CALCULATION:
![Bartlett](https://github.com/user-attachments/assets/e6609b87-cbb0-4af3-8470-121ba90dc2e6)

# OUTPUT:
<img width="471" height="474" alt="HPF-Bartlett Calculation" src="https://github.com/user-attachments/assets/fb14fcbe-c5ae-490e-bf4e-fcf44b2e94ed" />
<img width="770" height="723" alt="HPF-Bartlett graph" src="https://github.com/user-attachments/assets/0d59e629-4650-4d24-9272-1b7bf46d6762" />

# RESULT: 
Thus design of HIGH pass FIR digital filter using-Bartlett-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
``` 
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
Wc2=Wc(2); 
Wc1=Wc(1); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =(Wc2-Wc1)/%pi ; 
else 
hd(n) =((sin(Wc2 *((n -1)-alpha)))-(sin(Wc1 *((n -1)-alpha))))/(((n -1)-alpha)*%pi); 
end 
end 
// Bartlett Window 
for n = 1:M 
W(n)=1-((2*abs((n-1)-((M-1)/2)))/(M-1)); 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR BPF using Bartlett Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR BPF using Bartlett Window');
```
# CALCULATION:
![Bartlett](https://github.com/user-attachments/assets/4b40e38d-87a0-4a4f-8b2c-181bb264ff25)

# OUTPUT:
<img width="528" height="456" alt="BPF-Bartlett  Calculation" src="https://github.com/user-attachments/assets/483519bd-99b8-4867-a46b-91c3b41de5cf" />
<img width="757" height="721" alt="BPF-Bartlett Graph" src="https://github.com/user-attachments/assets/39bb8f7a-2727-4fc3-8d2c-0ea12137b221" />

# RESULT: 
Thus design of BAND pass FIR digital filter using-Bartlett-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
Wc2=Wc(2); 
Wc1=Wc(1); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =1-((Wc2-Wc1)/%pi); 
else 
hd(n) =((sin(Wc1 *((n -1)-alpha)))-(sin(Wc2 *((n -1)-alpha))))/(((n -1)-alpha)*%pi); 
end 
end 
// Bartlett Window 
for n = 1:M 
W(n)=1-((2*abs((n-1)-((M-1)/2)))/(M-1));  
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR BSF using Bartlett Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR BSF using Bartlett Window');
```
# CALCULATION:
![Bartlett](https://github.com/user-attachments/assets/a39ef3ec-2485-4fd1-a090-4ab715d3ad19)

# OUTPUT:
<img width="594" height="509" alt="BSF-Bartlett Calculation" src="https://github.com/user-attachments/assets/e882601d-854e-41e0-8666-66e2fcfe8eb9" />
<img width="755" height="716" alt="BSF-Bartlett Graph" src="https://github.com/user-attachments/assets/695cdb71-c196-44e3-81cc-2ab2e5b63650" />

# RESULT: 
Thus design of BAND STOP FIR digital filter using-Bartlett-Window waveforms were plotted and output was verified.
