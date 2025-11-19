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
```
import numpy as np
import matplotlib.pyplot as plt


Am=5.5
fm=467
fs=46700
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

Ac=11
fc=4670
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

am=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,am)
plt.show()



```

## Output Waveform

<img width="693" height="516" alt="image" src="https://github.com/user-attachments/assets/b3530331-8822-42e0-814e-e341d0c0f631" />




## Tabular Column

<img width="684" height="953" alt="image" src="https://github.com/user-attachments/assets/c065f113-89b8-4823-83c3-b0f4c17fc12c" />



## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
