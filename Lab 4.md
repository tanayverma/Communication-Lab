#2.Upsampling

We are sending information with L length

Our first bit will be our data, followed by L -1 zeroes where L is our length

```
e.g. For L = 5

+10000
```

#3.Pulse shaping

Each symbol we are transmitting is either 1 or -1, so

our root raised cosine pulse will have a filter outpuer in the **shape** of a root raised cosine pulse
