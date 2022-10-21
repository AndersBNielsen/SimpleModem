# SimpleModem
Simple Universal Modem

Check out the project on https://hackaday.io/project/186309-simple-universal-modem
Also check out the video demo: https://www.youtube.com/watch?v=k8hlYr6N3Ls

If you are looking for software to use with this, you should check out my 6502 Single Board Computer repo: https://github.com/AndersBNielsen/abn6502

TX:
The component values are configured to expect a 1200/2400Hz FSK modulated square wave on the DataOut(DOut on the silkscreen) pin. This signal is band pass filtered to make a 1V peak to peak sine wave that is output on the ModOut pin.

RX:
The ModIn pin expects an FSK modulated sine wave(Audio). 1V peak to peak recommended input. Output on the DataIn(DIn on the silkscreen) is a 5V square wave that can be used to decode the FSK decoding using an active low interrupt pin. The ModIn pin is not filtered but capacitively coupled using a 100nF cap. It's been tested using computer audio and tape with 1200/2400Hz FSK.

The TRRS jack's poles are meant to be configured using J1-J4 jumpers. An "iPhone" TRRS cable has the pinout right, left, GND, microphone - "Android" TRRS cable usually is right, left, microphone, GND. A standard TRS cable plugged into this would be right, left, GND, GND - for my 1972 tape deck I used a 3.5mm -> RCA/Phono cable and had it configured for ModIn, Modout, GND, GND. 
