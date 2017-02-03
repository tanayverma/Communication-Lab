#Exercise 1

* Convert letter from string (*ASCII binary representation*) to unsigned integer form 
* Treat each integer as a Fahrenheit value and convert to Celsius
* Average the Celsius values and compare to a predetermined "HOT" threshold value
* Output "HOT" if average value is higher than threshold


![](https://cloud.githubusercontent.com/assets/2521843/21977179/ff2158fa-dbcc-11e6-8f68-29a215bab123.png)



###Task

Input first 3 letters of surname

![](https://cloud.githubusercontent.com/assets/2521843/22104813/f3f5b016-de38-11e6-8ed8-ead6f11ea1b3.png)

Output

![](https://cloud.githubusercontent.com/assets/2521843/22104882/42f08b96-de39-11e6-9f4e-e4891731d030.png)

```cpp
The array contains the ASCII values for 'kue'

We then convert these values to fahrenheit and store them in an array

Lastly we get the average fahrenheit temp.

HOT turns on when its greater than or equal to 50
```

#Exercise 2 - CLT

This is the block diagram for the circuit :

![](https://cloud.githubusercontent.com/assets/2521843/22105642/ef1e3654-de3c-11e6-9296-36ad3f69869d.png)

This is the front panel:

![](https://cloud.githubusercontent.com/assets/2521843/22105610/cc334440-de3c-11e6-95c8-562b6eeda47e.png)

To create a Standard Normal distribution, our distribution must be normalised.

This is done by transforming the mean and standard deviation as follows:

Mean = 1/b-a

Standard Deviation :

![](https://cloud.githubusercontent.com/assets/2521843/22105116/7594a9a0-de3a-11e6-83cf-4cd9c0cfbf8c.png)


The part of the circuit that does this standardisation can be seen in the lower right corner of the loop. It takes away the mean (0.5) and and divides by the square root of the variance (12).




#Exercise 3 - Waveforms
Input
![](https://cloud.githubusercontent.com/assets/2521843/22105743/61bd94a2-de3d-11e6-8796-36be6e796270.png)

Output

The graphs show the waveform's PSD, the original waveform, and then the waveform after filtering.

The original waveform's FFT is also shown, with noticeable spikes at 10, 30 and 100Hz. After we applied a filter with a low cutoff of 25Hz and high cutoff of 35Hz, the FFT changes to show a spike at only 30Hz.

This concurs with the graph of the waveform post filter, as it is a sine wave with only one main frequency component at 30Hz.

This has happened because we have attenuated the two other frequency components that made up the original waveform with the filter.

![](https://cloud.githubusercontent.com/assets/2521843/22105958/6a4e836e-de3e-11e6-9ca2-2690570d32ed.png)


