
##### Item 1
> [!question] **Problem 1**
> An 8-bit ADC is used to digitize an analog signal with a range of 0V to 10V. The signal has a maximum frequency component of 3 kHz and is sampled at 12 kHz.
> >    1.1. How many quantization levels does the ADC have?
> >    1.2. What is the step size (volts per step) for this ADC?
> >    1.3. What is the Nyquist frequency for the given sampling rate?
> >    1.4. Will aliasing occur if the signal contains a frequency component at 7 kHz?
> >    1.5. Calculate the theoretical Signal-to-Noise Ratio (SNR) in dB for this ADC.

> [!note]+ Given
> $$\begin{flalign}
> & b = 8 \\
> & x_{max} = 10V \\
> &  x_{min} = 0V \\
> & f_{max} = 3 \ kHz \\
> & f_s = 12 \ kHz 
> \end{flalign}$$

> [!question]+ Required
> $$\begin{flalign}
> & 1.1. \ L \\
> & 1.2. \ \Delta \\
> & 1.3. \ f_N \\
> & 1.5. \ SNR_{dB}
> \end{flalign}$$

>[!done] 1.1 
>$$\begin{gathered}
L = 2^b \\
L = 2^8 \\
\boxed{L = 256 \ levels} \\
\end{gathered}$$

> [!done] 1.2
> $$\begin{gathered}
\Delta = \frac{x_{max}-x_{min}}{L-1} \\ \\
\Delta = \frac{10V-0V}{256-1} \\ \\
\boxed{\Delta = 39.22 \ mV \ per \ step} \\
\end{gathered}$$

> [!done] 1.3
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(3 \ kHz) \\\boxed{f_N = 6 \ kHz}
\end{gathered}$$

> [!done] 1.4
> $$\begin{gathered}
> \text{if} \ f_{max} = 7 \ kHz: \\
> f_N = 2f_{max} \\
> f_N = 2(7 \ kHz) 
> \\\boxed{f_N = 14 \ kHz} \\\\
> f_s \ge f_N, \; \text{no aliasing}\\
> \boxed{12 \ kHz < 14 \ kHz , \; \text{aliasing occurs}}
\end{gathered}$$

> [!done] 1.5
> $$\begin{gathered}
SNR_{dB} = 1.76 + 6.02b \\
SNR_{db} = 1.76 + 6.02(8) \\
\boxed{SNR_{dB} = 49.92 \ dB}
\end{gathered}$$

##### Item 2
> [!question] **Problem 2**
> You are working with a 12-bit ADC, converting a signal with a 0V to 5V range. The maximum signal frequency is 4 kHz, and the sampling rate is 10 kHz.
> > 2.1. What is the dynamic range of the 12-bit ADC in dB?
> >   2.2. What is the voltage step size for this ADC?
> >   2.3. Is the 10 kHz sampling rate sufficient to avoid aliasing?
> >   2.4. If aliasing occurs, what would be the frequency of the aliased component for a 6 kHz frequency signal?
> >   2.5. If the resolution is increased to 14 bits, what will be the new dynamic range?

> [!note]+ Given
> $$\begin{flalign}
> & b = 12 \\
> & x_{max} = 5V \\
> & x_{min} = 0V \\
> & f_{max} = 4 \ kHz \\
> & f_s = 10 \ kHz
> \end{flalign}$$

> [!question]+ Required
> $$\begin{flalign}
> & 2.1. \ DR_{dB} \ @ \ b = 12 \\
> & 2.2. \ \Delta \\
> & 2.4. \ f_{alias} \\ 
> & 2.5. \ DR_{dB} \ @ \ b = 14 
> \end{flalign}$$

> [!done] 2.1
> $$\begin{gathered}
DR_{dB} = 20log(2^b - 1) \\
DR_{dB} = 20log(2^{12} - 1) \\
\boxed{DR_{dB} = 72.25 \ dB} 
\end{gathered}$$

> [!done] 2.2
> $$\begin{gathered}
\Delta = \frac{x_{max}-x_{min}}{2^b-1} \\ \\
\Delta = \frac{5V-0V}{2^{12}-1} \\ \\
\boxed{\Delta = 1.22 \ mV}
\end{gathered}$$

> [!done] 2.3
> $$\begin{gathered}
> \text{if} \ f_{max} = 4 \ kHz: \\
f_N = 2f_{max} \\
f_N = 2(4 \ kHz) \\
f_N = 8 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{10 \ kHz > 8 \ kHz, \; \text{no aliasing}}
\end{gathered}$$
>> The 10 kHz sample rate is sufficient to avoid aliasing.

> [!done] 2.4 
> $$\begin{gathered}
f_{alias} = | kf_s - f_{signal}| \\ \\
f_{alias} = |(1 * 10 \ kHz) - 6 \ kHz| \\ \\
\boxed{f_{alias} = 4 \ kHz}
\end{gathered}$$

> [!done] 2.5
> $$\begin{gathered}
DR_{dB} = 20log(2^b-1) \\
DR_{dB} = 20log(2^{14} - 1) \\
\boxed{DR_{dB} =  84.29 \ dB}
\end{gathered}$$

##### Item 3
> [!question] **Problem 3**
An ADC with a 10-bit resolution is used to digitize a signal with a range of 0V to 8V. The signal contains frequency components at 2 kHz, 3.5 kHz, and 5 kHz. The sampling frequency is 15 kHz.
> > 3.1. How many quantization levels does the ADC have?
> > 3.2. Calculate the step size in volts.
> > 3.3. What is the Nyquist frequency for the given sampling rate?
> > 3.4. Will aliasing occur for the 5 kHz component? If so, at what frequency will the aliasing occur?
> > 3.5. What is the quantization error when digitizing a 4.5V input?

> [!note]+ Given
> $$\begin{flalign}
> & b = 10 \\
> & x_{max} = 8V \\
> & x_{min} = 0V \\
> & f_1 = 2 \ kHz \\
> & f_2 = 3.5 \ kHz \\
> & f_{max} = 5 \ kHz \\
> & f_s = 15 \ kHz
> \end{flalign}$$

> [!question]+ Required
> $$\begin{flalign}
> & 3.1. \ L \\ 
> & 3.2. \ \Delta \\
> & 3.3. \ f_N \\
> & 3.5. \ e_q \ @ \ v_i = 4.5V
> \end{flalign}$$

> [!done] 3.1
> $$\begin{gathered}
> L = 2^b \\
> L = 2^{10} \\
> \boxed{L = 1024 \ levels} 
> \end{gathered}$$

> [!done] 3.2
> $$\begin{gathered}
> \Delta = \frac{x_{max}-x_{min}}{L - 1} \\\\
> \Delta = \frac{8V - 0V}{1024 - 1} \\\\
> \boxed{\Delta = 7.82 \ mV}
> \end{gathered}$$

> [!done] 3.3
> $$\begin{gathered} 
> f_N = 2f_{max} \\
> f_N = 2(5 \ kHz) \\
> \boxed{f_N = 10 \ kHz}
> \end{gathered}$$

> [!done] 3.4
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(5 \ kHz) \\
f_N = 10 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{15 \ kHz > 10 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

> [!done] 3.5
> $$\begin{gathered}
> x[n] = 4.5 V \\
>\Delta = 7.82 \ mV \\\\\\
>x_q[n] = \left\lfloor \frac{x_{max} - x_{min}}{\Delta} \right\rfloor \times \Delta \\\\
>x_q[n] = \left\lfloor \frac{4.5V - 0V}{7.82 \ mV} \right\rfloor \times 7.82 \ mV\\\\
>x_q[n] = 575 \times 7.82 \ mV \\\\
>\boxed{x_q[n] = 4.500019 V} \\\\\\
>e_q = x[n] - x_q[n] \\
>e_q =  4.5V - 4.4965 V \\
>\boxed{e_q = 3.5 \ mV}
> \end{gathered}$$
##### Item 4
> [!question] **Problem 4**
An 8-bit ADC samples an analog signal with a 0V to 6V range. The signal has frequency components at 1 kHz, 2.5 kHz, and 3.5 kHz. The sampling frequency is 9 kHz.
> > 4.1. What is the voltage step size of the ADC?
> > 4.2. What is the Nyquist frequency for the given sampling rate?
> > 4.3. Will aliasing occur for the 3.5 kHz component? If so, at what frequency will aliasing occur?
> > 4.4. Calculate the theoretical Signal-to-Noise Ratio (SNR) for the 8-bit ADC.
> > 4.5. What is the dynamic range of the ADC in dB?

> [!given]+ Given
> $$\begin{flalign}
> & b = 8 \\
> & x_{max} = 6V \\
> & x_{min} = 0V \\
> & f_1 = 1 \ kHz \\
> & f_2 = 2.5 \ kHz \\
> & f_{max} = 3.5 \ kHz \\
> & f_s = 9 \ kHz
> \end{flalign}$$

> [!question]+ Required
> $$\begin{flalign}
> & 4.1. \ \Delta \\
> & 4.2 \ f_N \\
> & 4.4 \ SNR \ @ \ b=8 \\
> & 4.5 \ DR_{dB}
> \end{flalign}$$

> [!done] 4.1
> $$\begin{gathered}
> \Delta = \frac{x_{max}-x_{min}}{2^b-1} \\\\
> \Delta = \frac{6V - 0V}{2^8-1} \\\\
> \boxed{\Delta = 23.53 \ mV}
> \end{gathered}$$

> [!done] 4.2
> $$\begin{gathered}
> f_N = 2f_{max} \\
> f_N = 2(3.5 \ kHz) \\
> \boxed{f_N = 7 \ kHz}
> \end{gathered}$$

> [!done] 4.3
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(3.5 \ kHz) \\
f_N = 7 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{9 \ kHz > 7 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

> [!done] 4.4
> $$\begin{gathered}
> SNR = 1.76 + 6.02b \\
> SNR = 1.76 + 6.02(8) \\
> \boxed{SNR = 49.92 \ dB}
> \end{gathered}$$

> [!done] 4.5
> $$\begin{gathered}
> DR_{dB} = 20log(2^b - 1) \\
> DR_{dB} = 20log(2^8 - 1) \\
> \boxed{DR_{dB} = 48.13 \ dB}
> \end{gathered}$$

##### Item 5
> [!question] **Problem 5**
A 12-bit ADC is used to sample a signal with a range of 0V to 12V. The signal’s highest frequency component is 6 kHz, and the sampling rate is 20 kHz.
> > 5.1. What is the resolution of the ADC in terms of volts per step?
> > 5.2. Calculate the Nyquist frequency for the given sampling rate.
> > 5.3. Will aliasing occur for a frequency component of 10 kHz? If so, at what frequency will the aliasing occur?
> > 5.4. Determine the dynamic range of the 12-bit ADC.
> > 5.5. If the signal-to-noise ratio drops by 6 dB, what would be the new effective number of bits of the ADC?

> [!note] Given
> $$\begin{flalign}
> & b = 12 \\
> & x_{max} = 12V \\
> & x_{min} = 0V \\
> & f_{max} = 6V \\
> & f_s = 20 \ kHz
> \end{flalign}$$

> [!question] Required
> $$\begin{flalign}
> & 5.1. \ \Delta \\
> & 5.2 \ f_N \\
> & 5.4 \ DR_{dB} \\
> & 5.5 \ b_{eff} \ @ \ SNR_{12 \ bit} - 6dB
> \end{flalign}$$
>

> [!done] 5.1
> $$\begin{gathered}
> \Delta = \frac{x_{max}-x_{min}}{2^b-1} \\\\
> \Delta = \frac{12V - 0V}{2^{12}-1} \\\\
> \boxed{\Delta = 2.93 \ mV \ per \ step}
> \end{gathered}$$

> [!done] 5.2
> $$\begin{gathered}
> f_N = 2f_{max} \\
> f_N = 2(6 \ kHz) \\
> \boxed{f_N = 12 \ kHz}
> \end{gathered}$$

>[!done] 5.3
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(6 \ kHz) \\
f_N = 12 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{20 \ kHz > 12 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

>[!done] 5.4
> $$\begin{gathered}
> DR = 20log(2^b - 1) \\
> DR = 20log(2^{12} - 1) \\
> \boxed{DR = 72.25 \ dB}
> \end{gathered}$$

> [!done] 5.5
> $$\begin{flalign}
> \text{for} \ SNR_{12 \ bit}: \\
> & SNR_{12 \ bit} = 1.76 + 6.02b \\
> & SNR_{12 \ bit} = 1.76 + 6.02(12) \\
> & SNR_{12 \ bit} = 74 \ dB \\\\
> & 74 \ dB - 6 \ dB = 68 dB \\\\\\
> \text{For} \  b \ \text{when} \ SNR & = 68 \ dB: \\\\
> & b_{eff} = \frac{SNR-1.76}{6.02} \\\\
> & b_{eff} = \frac{68 \ dB - 1.76}{6.02} \\\\
> & b_{eff} = 11.00332 \\
> & \boxed{b_{eff} = 11 \ bits}
> \end{flalign}$$

##### Item 6
> [!question] **Problem 6**
A 10-bit ADC is used to digitize an analog signal ranging from 0V to 4V. The signal contains frequency components at 1.5 kHz, 2.5 kHz, and 5.5 kHz, and the sampling rate is 12 kHz.
> > 6.1. How many quantization levels does the ADC have?
> > 6.2. What is the voltage step size for this ADC?
> > 6.3. What is the Nyquist frequency for the given sampling rate?
> > 6.4. Will aliasing occur for the 5.5 kHz frequency component? If so, at what frequency will the aliasing occur?
> > 6.5. Calculate the theoretical SNR for this 10-bit ADC.

> [!note] Given
> $$\begin{flalign}
> & b = 10 \\
> & x_{max} = 4V \\
> & x_{min} = 0V \\
> & f_1 = 1.5 \ kHz \\
> & f_2 = 2.5 \ kHz \\
> & f_3 = 5.5 \ kHz \\
> & f_s = 12 \ kHz
> \end{flalign}$$

> [!question] Required
> $$\begin{flalign}
> & 6.1. \ L \\
> & 6.2. \ \Delta \\
> & 6.3. \ f_N \\
> & 6.5. \ SNR \\ 
> \end{flalign}$$

>[!done] 6.1
>  $$\begin{gathered}
>  L = 2^b \\
>  L = 2^{10} \\
>  \boxed{L = 1024}
> \end{gathered}$$

>[!done] 6.2
>$$\begin{gathered}
>\Delta = \frac{x_{max}-x_{min}}{L-1} \\\\
>\Delta = \frac{4V-0V}{1024-1} \\\\
>\boxed{\Delta = 3.91 \ mV}
>\end{gathered}$$

>[!done] 6.3
>$$\begin{gathered}
> f_N = 2f_{max} \\
> f_N = 2(5.5 \ kHz) \\
> \boxed{f_N = 11 \ kHz}
>\end{gathered}$$

>[!done] 6.4
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(5.5 \ kHz) \\
f_N = 11 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{12 \ kHz > 11 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

>[!done] 6.5
>$$\begin{gathered}
>SNR = 1.76 + 6.02b \\
>SNR = 1.76 + 6.02(10) \\
>\boxed{SNR = 61.96 \ dB}
>\end{gathered}$$
>

##### Item 7
> [!question] **Problem 7**
You are using an 8-bit ADC with a range of 0V to 3.3V to sample a signal with frequency components at 1 kHz, 2.8 kHz, and 4.5 kHz. The sampling rate is 10 kHz.
> > 7.1. What is the voltage step size of the ADC?
> > 7.2. Calculate the Nyquist frequency for the given sampling rate.
> > 7.3. Will aliasing occur for the 4.5 kHz frequency component? If so, what will be the aliased frequency?
> > 7.4. What is the quantization error when digitizing a 2V signal?
> > 7.5. If the signal-to-noise ratio is measured as 45 dB, how does it compare to the theoretical SNR for an 8-bit ADC?

>[!note] Given
> $$\begin{flalign}
> & b=8 \\
> & x_{max} = 3.3V \\
> & x_{min} = 0V \\
> & f_1 = 1 \ kHz \\
> & f_2 = 2.8 \ kHz \\
> & f_{max} = 4.5 \ kHz \\
> & f_s = 10 \ kHz
> \end{flalign}$$

>[!question] Required
>$$\begin{flalign}
>& 7.1. \ \Delta \\
>& 7.2. \ f_N \\
>& 7.4. \ e_q \\ 
>\end{flalign}$$

>[!done] 7.1
>$$\begin{gathered}
>\Delta = \frac{x_{max}-x_{min}}{2^b-1} \\\\
>\Delta = \frac{3.3V-0V}{2^8-1} \\\\
>\boxed{\Delta = 12.94 \ mV}
>\end{gathered}$$

>[!done] 7.2
>$$\begin{gathered}
>f_N = 2f_{max} \\
>f_N = 2(4.5 \ kHz) \\
>\boxed{f_N = 9 \ kHz}
>\end{gathered}$$

>[!done] 7.3
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(4.5 \ kHz) \\
f_N = 9 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{10 \ kHz > 9 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

>[!done] 7.4
> $$\begin{gathered}
> x[n] = 2 V \\
>\Delta = 12.94 \ mV \\\\\\
>x_q[n] = \left\lfloor \frac{x_{max} - x_{min}}{\Delta} \right\rfloor \times \Delta \\\\
>
>x_q[n] = \left\lfloor \frac{2V - 0V}{12.94 \ mV} \right\rfloor \times 12.93 \ mV\\\\
>x_q[n] = 155 \times 12.93 \ mV \\\\
>x_q[n] = 2.00415 V \\\\\\
>e_q = x[n] - x_q[n] \\
>e_q =  2V - 2.00415 V \\
>\boxed{e_q = -4.15 \ mV}
> \end{gathered}$$

>[!done] 7.5
>$$\begin{flalign}
>& SNR = 1.76 + 6.02b \\
>& SNR = 1.76 +6.02(8) \\
>& SNR = 49.92 \ dB \\\\
>& 49.92 \ dB - 45 \ dB = 4.92 \ dB \ \text{difference} \\\\
>& \text{Measured SNR} < \text{Theoretical SNR} \; \text{with} \ 4.92 \ dB \ \text{difference} \\
>& \boxed{ 45 \ dB < 49.92 \ dB}
>\end{flalign}$$
>>This could be due to noise, and other factors that can affect the effective number of bits

##### Item 8
> [!question] **Problem 8**
You are designing a system that uses a 14-bit ADC with a 0V to 5V input range. The maximum signal frequency is 3 kHz, and the sampling rate is 12 kHz.
> > 8.1. What is the resolution of the ADC in terms of volts per step?
> > 8.2. Calculate the Nyquist frequency for the given sampling rate.
> > 8.3. What is the theoretical SNR for this 14-bit ADC?
> > 8.4. If the SNR drops by 12 dB, how many effective bits would the ADC have?
> > 8.5. Calculate the dynamic range of the ADC in dB.

> [!note] Given
> $$\begin{flalign}
> & b=14 \\
> & x_{max} = 5V \\
> & x_{min} = 0V \\
> & f_{max} = 3 \ kHz \\
> & f_s = 12 \ kHz
> \end{flalign}$$

> [!question] Required
> $$\begin{flalign}
> & 8.1. \ \Delta \\
> & 8.2. \ f_N \\
> & 8.3. \ SNR \\
> & 8.4. \ b_{eff} \ @ \ SNR_{14 \ bit} - 12 \ dB \\
> & 8.5. \ DR_{dB}
> \end{flalign}$$

>[!done] 8.1
>$$\begin{gathered}
>\Delta = \frac{x_{max}-x_{min}}{2^b-1} \\\\
>\Delta = \frac{5V-0V}{2^{14}-1} \\\\
>\boxed{\Delta = 305.19 \ \micro V \ per \ step}
>\end{gathered}$$

>[!done] 8.2
>$$\begin{gathered}
>f_N = 2f_{max} \\
>f_N = 2(3 \ kHz) \\
>\boxed{f_N = 6 \ kHz}
>\end{gathered}$$

>[!done] 8.3
>$$\begin{gathered}
>SNR = 1.76 + 6.02b \\
>SNR = 1.76 + 6.02(14) \\
>\boxed{SNR = 86.04 \ dB}
>\end{gathered}$$

>[!done] 8.4
>$$\begin{gathered}
>b_{eff} = \frac{(SNR - 12 \ dB) - 1.76}{6.02} \\\\
>b_{eff} = \frac{(86.04 \ dB - 12 \ dB)-1.76}{6.02} \\\\
>b_{eff} = 12.00664 \\
>\boxed{b_{eff} = 13 \ bits}
>\end{gathered}$$

>[!done] 8.5
> $$\begin{gathered}
> DR_{dB} = 20log(2^b-1) \\
> DR_{dB} = 20log(2^{14}-1) \\
> \boxed{DR_{dB} = 84.29 \ dB}
> \end{gathered}$$

##### Item 9
> [!question] **Problem 9**
A 16-bit ADC is used to digitize an analog signal with a 0V to 10V range. The signal has frequency components at 2 kHz, 7 kHz, and 9 kHz, and the sampling rate is 18 kHz.
> >9.1. What is the voltage step size of the ADC?
> >9.2. Calculate the Nyquist frequency for the given sampling rate.
> >9.3. Will aliasing occur for the 9 kHz component? If so, what is the frequency of the aliased component?
> >9.4. Calculate the theoretical dynamic range for this 16-bit ADC.
> >9.5. What is the theoretical SNR for this ADC?

>[!note] Given
>$$\begin{flalign}
>& b = 16 \\
>& x_{max} = 10V \\
>& x_{min} = 0V \\
>& f_1 = 2 \ kHz \\
>& f_2 = 7 \ kHz \\
>& f_3 = 9 \ kHz \\
>& f_s = 18 \ kHz
>\end{flalign}$$

>[!question] Required
>$$\begin{flalign}
>& 9.1. \ \Delta \\
>& 9.2. \ f_N \\
>& 9.4. \ DR \\
>& 9.5. \ SNR 
>\end{flalign}$$

>[!done] 9.1
>$$\begin{gathered}
>\Delta = \frac{x_{max} - x_{min}}{2^b-1} \\\\
>\Delta = \frac{10V-0V}{2^{16}-1} \\\\
>\boxed{\Delta = 152.59 \ \micro V}
>\end{gathered}$$

>[!done] 9.2
>$$\begin{gathered}
>f_N = 2f_{max} \\
>f_N = 2(9 \ kHz) \\
>\boxed{f_N = 18 \ kHz}
>\end{gathered}$$

>[!done] 9.3
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(9 \ kHz) \\
f_N = 18 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{18 \ kHz = 18 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

>[!done] 9.4
>$$\begin{gathered}
>DR = 20log(2^b-1) \\
>DR = 20log(2^{16}-1) \\
>\boxed{DR = 96.33 \ dB}
>\end{gathered}$$

>[!done] 9.5
>$$\begin{gathered}
>SNR = 1.76 + 6.02b \\
>SNR = 1.76 + 6.02(16) \\
>\boxed{SNR = 98.08 \ dB}
>\end{gathered}$$

##### Item 10
> [!question] **Problem 10**
A 12-bit ADC is used with a signal having a 0V to 8V range. The signal contains frequency components at 1.2 kHz, 3 kHz, and 5 kHz. The sampling rate is 10 kHz.
> > 10.1. How many quantization levels does the ADC have?
> > 10.2. What is the voltage step size for this ADC?
> > 10.3. What is the Nyquist frequency for the given sampling rate?
> > 10.4. Will aliasing occur for the 5 kHz component? If so, at what frequency will the aliasing occur?
> > 10.5. If the SNR of the system is measured at 70 dB, how many effective bits does the ADC have?

>[!note] Given
>$$\begin{flalign}
>& b=12 \\
>& x_{max} = 8V \\
>& x_{min} = 0V \\
>& f_1 = 1.2 \ kHz \\
>& f_2 = 3 \ kHz \\
>& f_{max} = 5 \ kHz \\
>& f_s = 10 \ kHz 
>\end{flalign}$$

>[!question] Required
>$$\begin{flalign}
>& 10.1. \ L \\
>& 10.2. \ \Delta \\
>& 10.3. \ f_N \\
>& 10.5. \ b_{eff} \ @ \ SNR = 70 \ dB
>\end{flalign}$$

>[!done] 10.1
>$$\begin{gathered}
>L = 2^b \\
>L = 2^{12}\\
>\boxed{L = 4096 \ levels}
>\end{gathered}$$

>[!done] 10.2
>$$\begin{gathered}
>\Delta = \frac{x_{max}-x_{min}}{L-1} \\\\
>\Delta = \frac{8V-0V}{4096-1} \\\\
>\boxed{\Delta = 1.95 \ mV}
>\end{gathered}$$

>[!done] 10.3
>$$\begin{gathered}
>f_N = 2f_{max} \\
>f_N = 2(5 \ kHz) \\
>\boxed{f_N = 10 \ kHz}
>\end{gathered}$$

>[!done] 10.4
> $$\begin{gathered}
f_N = 2f_{max} \\
f_N = 2(5 \ kHz) \\
f_N = 10 \ kHz \\ \\
\text{if} \ f_s \ge f_N, \; \text{no aliasing} \\
\boxed{10 \ kHz = 10 \ kHz, \; \text{no aliasing}}
\end{gathered}$$

>[!done] 10.5
>$$\begin{gathered}
>b_{eff} = \frac{SNR - 1.76}{6.02} \\\\
>b_{eff} = \frac{70 \ dB - 1.76}{6.02} \\\\
>b_{eff} = 11.33555 \\
>\boxed{b_{eff} = 12 \ bits}
>\end{gathered}$$

