#Exercise 1 FM modulator - Change in frequency deviation

###Change in frequency = 500
![](https://cloud.githubusercontent.com/assets/2521843/22543861/55eb2c46-e92a-11e6-9583-563f3a9e259c.png)
###Change in frequency = 2000

![](https://cloud.githubusercontent.com/assets/2521843/22543885/6c83eab0-e92a-11e6-8d7a-7e012fd94cbc.png)

###Change in frequency = 5000
![](https://cloud.githubusercontent.com/assets/2521843/22543895/80431ca6-e92a-11e6-97bb-76e41913488d.png)


As we increase the frequency deviation the FM waveform has more visible compressions and rarefactions. The spread of values in the PSD also increases.

Frequency deviation is a measure of the statistical range of frequencies (the difference between lowest and highest frequencies). 

As this increases, naturally the PSD will reflect this by having spikes at a larger number of frequencies, as the FM signal is now made up of a more varied range of frequencies.


###Block diagram
![](https://cloud.githubusercontent.com/assets/2521843/22543826/2629a898-e92a-11e6-9f67-cb2a7fa2c381.png)

#Exercise 2 FM demodulator

###Block diagram
![](https://cloud.githubusercontent.com/assets/2521843/22567911/a3a37060-e989-11e6-877c-49519526f8f4.png)


#Top-level diagram

###Block diagram

![](https://cloud.githubusercontent.com/assets/2521843/22568115/73b67f5e-e98a-11e6-930c-97828612b155.png)

##FM simulation
###FM signal
![](https://cloud.githubusercontent.com/assets/2521843/22568473/e1aa5278-e98b-11e6-8cc0-c5eadf6b5090.png)

###Demodulated Time + PSD
![](https://cloud.githubusercontent.com/assets/2521843/22568533/0c6af198-e98c-11e6-8a3d-60912857c3b4.png)

>Our results are as expected, with the message signal having an amplitude of 2 and frequency at 1k Hz

#FM spectrum

##30k Freq Div
![](https://cloud.githubusercontent.com/assets/2521843/22586185/40fe7c1a-e9f3-11e6-96ce-dd1488319f68.png)
##5k Freq Div
![](https://cloud.githubusercontent.com/assets/2521843/22586213/5c58b426-e9f3-11e6-98c0-e49cba6ca15c.png)

> We can see that as we change our frequency our bandwwidth increase by a factor of 2 * (change in freq + B)
* I.E Around 12k for 5k Freq dev
* 62k for 30k  Freq dev
