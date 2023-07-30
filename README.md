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

### PHOTODIODE

Photodiode detect intensity of infrared light in surrounding.
Open current voltage: 0.39V
Max reverse voltage: 32V
Short-circuit current: 35 µA
Reverse light current: 25 to 35 µA when irradiance
1mW/cm2 for reverse voltage 5 V
Reverse dark current: 5 to 30nA considered as negligible
Raise time and fall time: 45ns
View angle: 80 degrees
Wavelength sensitivity: 940nm

#### PHOTODIODE CIRCUIT

![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/c65ba0ea-c76c-46a8-99a7-289adb843a37)

Since the Reverse Light current in range of nearly 25 µA
therefore Resistance is chosen as 200k Ω to get output voltage
in range of near 0 V during daytime.
Vout = 5 - IR or 5 - (25 µA ∙200k Ω) = 0 V (during daytime)
Vout = 5 - IR or 5 - (0 µA ∙200k Ω) = 5 V (during nightime)
The reverse light current value taken during daytime and night-time is an estimated value.

### Pyroelectric Sensor

Input: 5V DC
Output signal: 2V - 4V when HIGH
Sensing range: less than 120 degrees, within 7 meters 
Pyroelectric sensor output is connected to one of the AND gate terminals. The sensor is set as non-repeatable trigger i.e., when the output is high if the delay time is over, the output is automatically changed from high to low. Induction blocking time (the default setting: 2.5s blocked time): sensor module after each sensor output i.e., from high to low is followed by a blockade set period of time, during this time period sensor does not accept any sensor signal.

#### Pyroelectric motion sensor

![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/28fcb2c1-f981-47f2-a35e-a24fc3691422)

### RELAY MODULE

Operating Voltage 5 V
Operating current 20 mA
Maximum switching voltage 250 VAC 10 A; 30 VDC 10A
Operating time is 10 ms
Release time is 5 ms
The 5 V 1 channel relay single pole double throw (SPDT) is used as normally open relay. It is connected in series with the wire as a switch of light bulb. The disadvantage of this relay module is it may damage if it is used overtime. Since we are only using this module for few minutes it should work for long period of time.

![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/7eea9384-4a6b-41ae-b46e-70a64cb1f4cd)
#### 5 V 1 channel relay module to switch on and off light

## PROJECT IMPLEMENTATION IDEA

In the building, between two floor there are staircase containing one light then we require two pyroelectric sensors placed at starting point and ending point of staircase. The two pyroelectric sensor signal is connected to OR gate, output of OR gate is considered as final motion sensor signal for switching light. The 7 floors would require 7 such pyroelectric sensors one in each floor. Also, we would require 6 such switching circuits to switch the light. Therefore, n floor building we would require n pyroelectric sensors and n-1
switching circuits.

This model can further be improved if we introduced a wireless communication between the switching circuits and pyroelectric sensors. The complexity of wire and the requirement of long wire to connect pyroelectric sensor module which would be kept far apart is reduced. For wireless communication a radiofrequency transmitter and receiver for example 433MHz Transmitter Receiver Wireless module can be used which consumes low power and has a transmit range up to 50 m which is enough for transmitting signal.

### PROJECT IMAGE

#### Light off, no motion detected.
![image](https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/cfb8de0e-a4a6-4d15-8f1b-17ff6050241e)

#### Light on, when a motion is detected
(https://github.com/ashwini0921/Automatic-Staircase-Light-Switching-at-Night/assets/111654188/8f40ca43-8a76-42d9-b9f6-b9862a868cf6)

## CONCLUSION

In this project circuit to switch on and off the staircase light at night when motion is detected is designed. The intension of this projectis to tackle the problem of unnecessary wastage of energy caused when light is kept on for whole night. The project can also be implemented as a step to automate building or home. The design is cost effective estimated INR 550 for a single model. The need of microcontroller is eliminated by the use of 555-timer and IC7408 AND gate, the microcontroller is quite expensive and only few features of microcontroller are utilized in this model. Hence, it’s not only saving energy but also money.

## ACKNOWLEDGMENT

I would like to thank my ECE analog faculty to give me this wonderful opportunity to design this project on “Automatic staircase light switching at night”. I would like to thank all my school teachers as well as my 1st year college teachers who made me capable of designing this project. I would also like to give special gratitude to my parents who financially supported me to complete this project.

## REFERENCES


[1] https://www.ti.com/lit/ds/symlink/lm555.pdf.

[2] https://www.electronics-tutorials.ws/waveforms/555_timer.html

[3] https://www.electronicsforu.com/resources/photodiodeworking-applications

[4] https://www.mpja.com/download/31227sc.pdf

[5] https://www.elprocus.com/5v-relay-module/

[6] https://circuitdigest.com/electronic-circuits/and-gate-circuitworking

[7] Microelectronic circuits Book by Adel Sedra and Kenneth C.
Smith

[8] Kuri, Rahul & Chakraborty, Atanu & Sanyal, Judhajit. (2019). Automatic Switching System for Streetlights. IJIREEICE. 7. 101-102.
10.17148/IJIREEICE.2019.7416.

[9] Dixit, Kratika. (2019). AUTOMATIC ROOM LIGHT SYSTEM FOR POWER SAVING.




