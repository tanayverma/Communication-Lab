#Lab 4 - Exercise 1 - BPSK Transmitter

>Number of samples per symbol, L = 10 (The Symbol rate / message length)

##What is the root-raised cosine filter?

A filter that meets the Nyquist ISI criterion - that results in no intersymbol interference.

##What is the decimate function?

The decimate function divides the elemnts of array into output arrays, placing elemnts into outputs successively.

When we transmit consecutive symbols the impulse resposne causes a sybol to transmit causes intersymbol inteference.
##Block diagram 
![](https://cloud.githubusercontent.com/assets/2521843/22629581/897bd7b4-ebe0-11e6-8330-0e5963bec3b9.PNG)


##Output waveform
![](https://cloud.githubusercontent.com/assets/2521843/22642094/324b9daa-ec51-11e6-81fb-301a78c7bf71.png)

##Graph root-raised cosine
![](https://cloud.githubusercontent.com/assets/2521843/22641988/c991db08-ec50-11e6-8705-2882dbe341ad.png)

Our mainlobe bandwidth is around 8kHz

##Graph - No pulse shaping
![](https://cloud.githubusercontent.com/assets/2521843/22642066/1478c38e-ec51-11e6-8be0-c4ab8511f456.png)

The shape of the filter suggests that it could be a first-order filter - cutting off the high frequency components and acting like a low pass filter.

#Exercise 2 - BPSK Receiver

##Block diagram
![](https://cloud.githubusercontent.com/assets/2521843/22629583/8fc1806a-ebe0-11e6-8055-a0422c5ea010.PNG)

##Demodulated signal
![](https://cloud.githubusercontent.com/assets/2521843/22629584/8fc209e0-ebe0-11e6-8453-bd159e806d26.PNG)

The BER (Bit error rate) we obtained for the transmitter ranged from

0.004769 - 0.336364, which was a very big range. This might have been due to the non-ideal nature of the filter.

For the different gains for Tx and Rx, we obtained BER values ranging from 0.49-0.51 which is non-ideal.

For transmitting bits this system does not perform well.

##Exercise 3 Error Correction Coding

##Changed block
![](https://cloud.githubusercontent.com/assets/2521843/22644624/3642aed0-ec5b-11e6-9af4-016024d1baaa.png)

We added the C code provided but it would not run due to an internal error.



![](https://cloud.githubusercontent.com/assets/2521843/22644689/6aec2daa-ec5b-11e6-89d8-16262fc4091a.png)
#DPSK

##Block diagram

![](https://cloud.githubusercontent.com/assets/2521843/22646121/97af7246-ec62-11e6-9483-dfbe479b7984.png)

We obtained BER values of ~0.42 which we believe is better than the BPSK which we obtained a value of around 0.5

This is slightly better and it shows DPSK has more noise resilience compared to BPSK. This is because the differentiation fuction compares only the difference between the bits which reduces the impact of noise.
