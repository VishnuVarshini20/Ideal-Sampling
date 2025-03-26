# **Ideal Sampling**

# **M. Vishnu Varshini**
# **212223060306**

**Aim:**

To study and perform the construction and reconstruction of impulse or ideal sampling and observe the sampled waveform.

**Tools Required:**

Python IDE with Numpy and Scipy

**Program:**

```
#Impulse Sampling
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
**Output:**

![impulse1](https://github.com/user-attachments/assets/2d33490d-96fd-4e60-8dbd-f43f8aa1f3d7)
![impulse2](https://github.com/user-attachments/assets/0a8a36fd-81f2-416d-846a-87a69378a863)
![impulse3](https://github.com/user-attachments/assets/a5ec5ae4-6594-472d-a3a0-5986637a7eaa)

**Result:**

The construction and reconstruction of impulse (ideal) sampling using Python were successfully verified.





