# Aether Plane Take off
Forensics 724 pts -> Solve by Sarastro.

Even though they classified it under Forensics I still think it falls under a different branch. The Aether Plane Take Off challenge is the highest ranking challenge but it's really easy if u have experience or just get lucky.

## Forensic Enumeration
Now since it is a forensics challenge we thought we would need to check the file, analyze it hard, binwalk it and others but upon doing every enumeration we could, we just found out it is a normal .wav file.

We ploncked it Sonic Visualier to check the frequency waves as well to see if there are any hidden messages but still nothing. 

We continued analyzing it to see if we could get anything from it and upon seeing the waves, running it through frequency analyzers and similar wave enumeration methods, we got that the message is PSK encrypted.

Eventually getting EssexPSK, a PSK and RTTY reciever that decodes a message, we worked our way towards the flag.

Downloading it we came across a problem. It only read through the microphone, so we made a vbcable virtual connection for my headset to act as a microphone in the program. We also had to change up the frequency a bit to match the RX return value.

![Screenshot_1](https://user-images.githubusercontent.com/74470185/99834180-77681a80-2b63-11eb-909e-af67a9c8f5c6.png)

Ran it and got the flag!
