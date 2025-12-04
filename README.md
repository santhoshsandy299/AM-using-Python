# AM-Using-Python
## Aim
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

## Apparatus Required
Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer
## Theory
Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:

## Algorithm
Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
Generate Time Axis: Create a time vector for the signal duration.
Generate Message Signal: Define the message signal as a cosine wave.
Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.
## Program
```
import numpy as np
import matplotlib.pyplot as plt


Am=5.3
fm=447
fs=44700
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

Ac=10.6
fc=4470
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

am=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,am)
plt.show()

```


## Output Waveform
<img width="784" height="640" alt="image" src="https://github.com/user-attachments/assets/4dc45713-1ae1-4258-b71d-48105843bc2c" />
## Tabulation
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/4417b736-fc49-4760-8c20-370b68c75d28" />


## Result
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
