# Multirate Signal Processing- Decimation and Interpolation
#          Multirate Signal Processing- Decimation and Interpolation
# AIM: 
          
  To perform decimation and interpolation operations on a disctrete time signal and study the spectrum using SCILAB 

# APPARATUS REQUIRED: 

  PC Installed with SCILAB 

# PROGRAM for Decimation and Interpolation
```
clc; clear; close;

// Original signal Fs = 1000; // Sampling frequency f = 100; // Signal frequency t = 0:1/Fs:0.1;

x = sin(2*%pift);

// ---------------- DECIMATION ---------------- M = 2; // Decimation factor

// Low-pass filtering before downsampling fc = Fs/(2*M); N = 50;

h = zeros(1,N+1);

for n = 0:N if n == N/2 then h(n+1) = 2fc/Fs; else h(n+1) = sin(2%pifc/Fs(n-N/2)) / (%pi*(n-N/2)); end end

// Apply filter y = convol(x,h);

// Downsample x_dec = y(1:M:$);

// ---------------- INTERPOLATION ---------------- L = 2; // Interpolation factor

// Insert zeros x_int = zeros(1,length(x_dec)*L);

x_int(1:L:$) = x_dec;

// Low-pass filter after interpolation fc2 = Fs/(2*L);

h2 = zeros(1,N+1);

for n = 0:N if n == N/2 then h2(n+1) = 2fc2/Fs; else h2(n+1) = sin(2%pifc2/Fs(n-N/2)) / (%pi*(n-N/2)); end end

// Apply interpolation filter x_interp = convol(x_int,h2);

// ---------------- PLOTS ----------------

scf(1);

// Original signal subplot(3,1,1); plot(t,x); xtitle("Original Signal","Time","Amplitude");

// Decimated signal subplot(3,1,2); plot(x_dec); xtitle("Decimated Signal (M = 2)","Samples","Amplitude");

// Interpolated signal subplot(3,1,3); plot(x_interp); xtitle("Interpolated Signal (L = 2)","Samples","Amplitude");
```



# OUTPUT and spectrum for Decimation and Interpolation
<img width="1320" height="707" alt="image" src="https://github.com/user-attachments/assets/514e8b00-6947-410d-b11d-5873bc0005d3" />
# Result
Thus, The code for Multirate Signal Processing- Decimation and Interpolation was run successfully


# RESULT
