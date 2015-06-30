# HeatbeatDetector
Test program for an algorithm to detect heartbeats using a microphone
DetectorTest.pd is a PureData patch to test an algorithm for detecting heartbeats using a microphone. 
The goal is reliable detection of the heartbeat regardless of microphone level, noise, or poor frequency response.
Current performance:
1.  Level independency: Accurate count with input level from 0dB to -80dB with no manual adjustment
2.  Noise rejection:  Accurate count with signal to noise ratio of 20dB
3.  Accurate count despite 3dB per octave highpass filter in microphone.  Cutoof can be varied from 1 to 400Hz without decreasing accuracy.

High noise levels do not influence the count, but do cause inaccuracies in the onset detection.  
HRV measurements not possible at higher noise levels.

When the heartbeat detector is adjusted for high noise levels, it will accurately detect heartbeats at lower noise level.
It will in this case, though, detect false hearbeats when there is no signal.
