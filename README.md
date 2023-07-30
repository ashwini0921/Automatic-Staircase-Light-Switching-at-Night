# Automatic-Staircase-Light-Switching-at-Night
Analog Electronic Circuit Project

## ABSTRACT
In big flats, it is difficult to switch off all the light by a person at late night. The people who work on afternoon reach resident nearly midnight so it causes inconvenience for them to walk up the staircase in dark. In order to avoid this the lights in the staircase are kept on, this causes wastage of energy. A motion sensor can be used to detect person. If the sensor detect any motion and it is dark then the light is switched on using relays. To detect whether it is dark or not, a photodiode or LDR can be used. If the motion sensors do not detect any motion for around 2 min, then it automatically switched off, the 555-timer designed in monostable multivibrator configuration switch off
the relay after 2 min.

## INTRODUCTION
The motion detector (Pyroelectric Sensor) detects a change in infrared radiation of two segments of the sensor. The human body emits infrared radiation of wavelength mainly in 12 microns with low intensity. When a person moves toward the sensor the intensity of infrared radiation falling in one segment is more than the other segment and vice versa when a human moves away from the sensor. The sensor detects this change and sends a signal as “HIGH” to the 555-timer. Photodiode absorbs light or photons to create pair of electrons and holes. The infrared light is converted to an electrical signal using a photodiode. It can be used to determine whether it is night or
not. If it is night time, it will send a signal as “HIGH” to the 555-timer. The relay is used to turn on the switch when it receives a signal from the 555-timer. It works on principle electromagnetic induction. The relay switch on the light bulb which is connected to mains. In order to make the complete circuit independent of the external power source like batteries, the power from mains can be used as a power source for this circuit, in order to achieve this an AC to DC converter is used. The pyroelectric sensor detects the motion in staircase. Photodiode sends signal as HIGH if it is night time. If the pyroelectric sensor detects any motion, it would send signal to
AND logic gate which check whether pyroelectric signal as well as photodiode is HIGH or not. If both of it are logically
HIGH then the monostable multivibrator switch on the relay for 2 min. After 2 min the light is again switched off. This process is repeated again.

## 
