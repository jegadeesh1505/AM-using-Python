# AM-using-Python

## Aim


To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:



## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program

```python
import numpy as np
import matplotlib.pyplot as plt
Am=6.2
fm=495
Ac=12.4
fc=4950
fs=49500
t= np.arange(0, 3/fm, 1/fs)

m=Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

s=(Ac+m)*np.cos(2*3.14*fc*t)
plt.subplot(3,1,3)
plt.plot(t,s)

```

## Output Waveform

<img width="691" height="518" alt="Screenshot 2025-11-09 225042" src="https://github.com/user-attachments/assets/77e82927-57ee-4716-b638-b5eb786f2b63" />

## Tabular Column

![WhatsApp Image 2025-11-09 at 22 46 14_817bfbc8](https://github.com/user-attachments/assets/c34692ff-5e7e-4c21-8800-b25e08caa818)

## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
