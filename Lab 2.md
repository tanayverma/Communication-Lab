#Exercise 1: AM Modulation

![](https://cloud.githubusercontent.com/assets/2521843/22418782/56e8c112-e6d2-11e6-947e-364ff845c1ce.png)



![](https://cloud.githubusercontent.com/assets/2521843/22418832/9b02224e-e6d2-11e6-9510-a753477ebeeb.png)

##Modulation index = 0.5
![](https://cloud.githubusercontent.com/assets/2521843/22418915/fbb14ac0-e6d2-11e6-9737-e33737ac3c42.png)

##Modulation index = 1
![](https://cloud.githubusercontent.com/assets/2521843/22418936/144243b4-e6d3-11e6-8556-98e53970b8ba.png)

##Modulation index = 1.5

![](https://cloud.githubusercontent.com/assets/2521843/22418963/2cf2ddc4-e6d3-11e6-96db-915a855ae067.png)

###Impact of modulation index on modulated signal?

The modulation index is equal to Amplitude(message)/Amplitude(carrier), so it is a representation of how similar the AM waveform is to the message signal. 

Increasing the modulating index will make the signal more like the original sinewave, as shown by each successive AM Power Spectrum having larger spikes centred around the main 10kHz spike.


###Effect of changing frequency to 1k,2k,5k (same modulation index)

###1k

![](https://cloud.githubusercontent.com/assets/2521843/22419099/cc80b848-e6d3-11e6-8e0f-6c785027d946.png)

###2k
![](https://cloud.githubusercontent.com/assets/2521843/22419138/fdefda4e-e6d3-11e6-9754-06afac5a15b9.png)

###5k
![](https://cloud.githubusercontent.com/assets/2521843/22419166/1dee6ed2-e6d4-11e6-87c5-c263fa1bcbdf.png)


Increasing the frequency of the message signal brings the range of frequencies of the AM waveform closer to the frequency of the carrier signal, causing the AM waveform to look increasingly like a sine wave of frequency 10kHz. 

#Exercise 2A - COHERENT DETECTION

![](https://cloud.githubusercontent.com/assets/2521843/22419295/b74bad38-e6d4-11e6-851e-7a423c6d8fe1.png)

###Explain mathematical theory behind this demodulation. Why low pass and why - DC? Why do we need to scale the message?

The message signal is m(t). The carrier signal is cos(wct). The AM signal is the message x carrier =  m(t)cos(wct). 

When the AM signal is multiplied again by the carrier, it becomes m(t)cos^2(wct). This is mathematically equivalent to 0.5[m(t) + m(t)cos(2wct). 

The fourier transform of this = 0.5M(w) + 0.25[M(w + 2wc) + M(w - 2wc)]. This means there are three peaks centred around frequencies of 0, 2wc and -2wc. We use a low pass filter to remove the peaks at 2wc and -2wc, leaving only 0.5M(w).

Removing the DC component after the filter eliminates the carrier signal, meaning the signal is now 0.5m(t). This is then scaled up by 2 to get the original message signal, m(t).



#Exercise 2B - ENVELOPE DETECTION
![](https://cloud.githubusercontent.com/assets/2521843/22419380/21913f78-e6d5-11e6-81a3-c26300a94116.png)

###Explain the mathematical theory

The message signal = m(t). The modulating signal = A + m(t). The modulated signal = [A + m(t)]cos(wct).

For envelope detection to work, A + m(t) >= 0. This is why we have a case structure which takes all negative values of the signal and sets them to 0, meaning the signal is always >= 0.

This signal can then be demodulated using the method in the exercise above, using a filter and by removing the DC component.



#Exercise 3 - AM SIMULATION
![](https://cloud.githubusercontent.com/assets/2521843/22419458/7dd9865a-e6d5-11e6-84f6-fc03ed1eae67.png)


![](https://cloud.githubusercontent.com/assets/2521843/22419592/24d12a62-e6d6-11e6-9aba-1da10ab6a1ba.png)

###Message amplitude : 1

![](https://cloud.githubusercontent.com/assets/2521843/22420043/3636f9f6-e6d8-11e6-8738-2cab69c3f6cc.png)
###Message amplitude : 2

![](https://cloud.githubusercontent.com/assets/2521843/22420074/5c8ae522-e6d8-11e6-95fb-28b349d0f4c7.png)

###Message amplitude : 3
![](https://cloud.githubusercontent.com/assets/2521843/22420096/7aecd3d6-e6d8-11e6-8b94-cdcde344d05a.png)


###Message amplitude : 4
![](https://cloud.githubusercontent.com/assets/2521843/22420130/a5572e00-e6d8-11e6-83c9-b7de7c4e8e9e.png)

###Explain any changes between the two modulation techniques as the message signal amplitude changes from 1 to 4 with steps of 1

The only difference between the two detection technquies is that as the message amplitude increases, the PSD of the Envelope Detected waveform starts to show two small peaks at 2k and 3k, apart from the much larger peak at 1k. 

This is most likely due to the fact that Envelope Detection is more prone to noise than Coherent Detection.

#Ex 4 - AM COMMUNICATIONS VIA USRP

###Explain how transmitter and reciever works.

###Revise usrp

