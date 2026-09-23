# zx
This is just mostly for personal documentation but may be useful to some. I cant guarantee any of this will result in a working ZX tape file. 

information on how to decode .wav to .tzx

Because it took several hours of research on how to decode a tape I found in a pile of used cassette tapes, this seems like a fun hobby

First you may do a bit of audio prepping - 

## Remove DC Offset 

One you have a .wav file imported, you will probably have some DC Offset.

Fix this by importing .wav into Audacity 

Effects >> Volume and Compression >> Normalize
- Check Remove DC Offset

##

Effects >> EQ and Filters >> High-Pass Filter
- Set 300Hz and 12dB roll-off 

Export your new audio file as .wav

## Convert
audio2tape converts audio files to ZX Spectrum tape images.

This was the strongest tool ive found thus far for my needs. Simply run a conversion command:
```
audio2tape -t schmitt -z 127 -c 12 tape.wav tape.tzx
```

## Emulate

Then take tape.tzx and drop it in a ZX Spectrum emulator

There are several in the wild but I like ZEsarUX

download ZEsarUX:
https://github.com/chernandezba/zesarux

## Thats it! (?)

if i find any tapes in the wild and I am allowed to share a working tape file I will link it here!
