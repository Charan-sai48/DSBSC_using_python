# DSBSC_using_python
## Aim
To implement and analyze DSBSC modulation and demodulation using Python's NumPy and Matplotlib libraries.

## Apparatus Required

Software: Python with NumPy and Matplotlib libraries<BR>
Hardware: Personal Computer

## Theory

Double Sideband Suppressed Carrier (DSBSC) modulation is a type of amplitude modulation in which the carrier signal is suppressed, and only the two sidebands containing the information are transmitted. In DSBSC, the transmitted signal consists of the upper sideband (USB) and the lower sideband (LSB) components, which carry the same information as the carrier but without wasting power on the carrier itself.

## Algorithm

Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.

Generate Time Axis: Create a time vector for the signal duration.

Generate Message Signal: Define the message signal as a cosine wave.

Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.

Generate DSBSC Signal: Apply the DSBSC modulation formula to obtain the modulated signal.

Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signals.

## Program 
```
import numpy as np
import matplotlib.pyplot as plt

Am = 5.7
fm = 497
Ac = 11.4
fc = 4970
fs = 49700

t = np.arange(0, 0.01, 1/fs)

message = Am * np.cos(2 * np.pi * fm * t)
carrier = Ac * np.cos(2 * np.pi * fc * t)
dsbsc = message * carrier

plt.figure(figsize=(10, 6))

plt.subplot(3, 1, 1)
plt.plot(t, message)

plt.subplot(3, 1, 2)
plt.plot(t, carrier)

plt.subplot(3, 1, 3)
plt.plot(t, dsbsc)

plt.tight_layout()
plt.show()

```
## Output

<img width="1241" height="739" alt="Screenshot 2025-11-16 194209" src="https://github.com/user-attachments/assets/045e81cd-e29c-44f4-86ce-f47846bce45f" />

## Tabular Column

## Result
