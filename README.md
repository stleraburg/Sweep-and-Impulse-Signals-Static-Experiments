# Comments

The experiments were conducted with a gripper compressing a silicon and a plastic cubes with a constant force of 1N. The vibromotor was located within the RIGHT finger. Both accelerometers were connected 
to the internal ADCs of STm32.

1. Sweep (Chirp) signal signal generation is highly dependent on the clock of STm32F4 microcontroller's clock. To change the frequency of the output sine wave, the Prescaler value has to be changed accordingly.
  Because the Prescaler can only be an integer number, the smooth transition of frequencies is only possible within the range between 100 and 300 Hz. As for the higher frequencies,
  the sweep signal cannot take all frequencies in a range, resulting in discountinuous output.

**Input Signals and Their FFT: data from oscilloscope**

![alt text](https://github.com/stleraburg/Sweep-and-Impulse-Signals-Static-Experiments/blob/master/100-250input.png)
![alt text](https://github.com/stleraburg/Sweep-and-Impulse-Signals-Static-Experiments/blob/master/200-300input.png)
![alt text](https://github.com/stleraburg/Sweep-and-Impulse-Signals-Static-Experiments/blob/master/300-450input.png)

2.  The vibromotors are not powerful enough to produce impulse signal and get the desired output. The signal received by accelerometers is very weak.
    The minimum pulse width produced by the microcontroller is 40ms. 
