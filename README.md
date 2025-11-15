# Design-of-FIR-Filters-using-rectangular-window
#          DESIGN OF LOW PASS FIR DIGITAL FILTER 

# AIM: 
          
  To generate design of low pass FIR digital filter using SCILAB 

# APPARATUS REQUIRED: 

  PC Installed with SCILAB 

# PROGRAM 
```
clc;
clear;
close;


forder = 33;                     
cutoff_frequency = 0.2;          
window_type = "hm";              
window_params = [0, 0];          

[h, h_freq, fr] = wfir("lp", forder, [cutoff_frequency, 0], window_type, window_params);


disp(h, "Filter Coefficients:");

scf(0);
subplot(2,1,1);
plot(fr, abs(h_freq));
xlabel("Normalized Frequency");
ylabel("Magnitude");
title("Frequency Response Magnitude of FIR Low Pass Filter");


subplot(2,1,2);
plot(fr, 20*log10(abs(h_freq)));
xlabel("Normalized Frequency");
ylabel("Magnitude (dB)");
title("Frequency Response (dB) of FIR Low Pass Filter");
```

# OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e014cd3f-1591-4d6c-abef-c7b65435ebb3" />

# RESULT

THE DESIGN OF LOW PASS FIR DIGITAL FILTER IS SUCCESSFULLY COMPLETED USING SCILAB.
