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

## PROJECT DESIGN

The diagram in Fig 1 shows the design model. The power from main is step down and converted to 5 V DC the 5 V DC which is VCC pyroelectric sensor and photodiode send signal to 555 timer monostable multivibrator configuration which send the signal to Relay module as HIGH for 2 min if both pyroelectric sensor signal and photodiode signal is HIGH. The Relay switch on power to light used in staircase.

#### CIRCUIT BLOCK DIAGRAM
![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/43af6b8f-6026-4f65-b9fe-a74ad2b02f7e)

### MONOSTABLE CONFIGURATION

#### The Circuit diagram of pyroelectric sensor signal and signal from photodiode connected to 555-timer in monostable multivibrator configuration.

![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/add33f59-8db0-4db3-a9b3-6f9875fca44e)

The duration of on or Time Period is given by T=1.1R1C2 Resistor R1 is chosen as 100kΩ and Capacitor C2 chosen as 1000µF which gives T=1.1∙100kΩ ∙1000µF or 110 s. The transistor acts like a switch when output of AND gate is logically HIGH i.e. 5 V the voltage of trigger is nearly zero, thus creating negative voltage impulse and the timer begins.

#### The LT spice Circuit of NE555 Circuit

![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/0f6298e4-c412-4132-b196-f325a3e0abca)

Since the NE555 model used in LT spice is different hence is not same when 100k Ω resistor is used. Instead 135k Ω resistor provides the correct output for LT spice model.

#### LT spice Simulation Output:

![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/ab797cda-28c6-43d2-b546-3946593553b2)



