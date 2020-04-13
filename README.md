# LIGHT-OPERATED-LOCK
Using LOL we can unlock,lock the door of the room remotely from our bed. 
Using light operated door latch circuit, we can close or open the door of our room remotely from our bed. We just have to focus the torchlight on the light dependent resistor of the circuit, which we can install inside our room at a suitable position.

![](https://github.com/Sankul2699/LIGHT-OPERATED-LOCK/blob/master/Images/Screenshot%20(47).png)

![](https://github.com/Sankul2699/LIGHT-OPERATED-LOCK/blob/master/Images/door%20unlock.JPG)

## Video Demonstration
In the video the stepper motor is represented like a fan connected to a motor just to show the direction of the rotation.
The stepper motor is later connected to the latch to lock and unlock door.The latch motor  interface was not made at the time of making this video. 
[Light Operated door lock](https://www.youtube.com/watch?v=VgwU3S13_K8)

# Circuit diagram
 
![](https://github.com/Sankul2699/LIGHT-OPERATED-LOCK/blob/master/Images/CKT%20diag.PNG)
Fig. 1: Light operated door latch: control unit

The circuit comprises a control unit and a driver unit for the stepper motor circuit used to latch/open the door. 
The control unit comprises two timer 555 ICs (IC1 and IC2), NAND gate IC (IC3), 4-bit bidirectional universal shift register (IC4), OR gate (IC5), NOR gate (IC6), hex inverter (IC7) and dual D-type positive-edge triggered flip-flop (IC8) as shown in Fig. 1. The driver circuit shown in Fig. 2 uses four Darlington pair transistors (T1 through T8) to increase the current carrying capability for operating the stepper motor.

The astable multivibrator built around timer 555 (IC1) has a time period of 1.5 seconds. The monostable built around IC2 is triggered when torchlight is focused on light-dependent resistor LDR1. Sensitivity potentiometer VR1 is adjusted to ambient light. Normally, the LDR is kept covered to avoid its activation by ambient light.

![](https://github.com/Sankul2699/LIGHT-OPERATED-LOCK/blob/master/Images/darligtonpair_transistors.JPG)

Fig. 2: Light operated door latch: Driver circuit for the stepper motor
# Circuit operation

When torchlight is focused on the LDR, the monostable (IC2) is triggered. The ‘on’ time of IC2 is adjusted to 15 seconds by potentiometer VR4. The outputs at pin 3 of astable IC1 and monostable IC2 are fed to NAND gate N1 of IC3. The Q0 and Q1 outputs of shift register IC4 are ORed by OR gate N2 and its output is fed to NOR gate N3. The Q2 output of IC4 forms the second input for NOR gate N3. The output of NOR gate N3 goes to shift-right and shift-left serial data inputs (pins 2 and 7) of IC4.

Mode-control inputs S0 and S1 are used for direction changing of shift register IC4. The Q1 output of dual D-type flip-flop IC8 is fed to S0 directly and to S1 after inversion by N4.
The output of monostable IC2 resets IC4 via resistor R4, which stops the stepper motor..
The monostable output also provides clock to the D flip-flop operating in toggle mode by connecting Q1 to D1 of IC8.
Fig. 2 shows the driver unit for the stepper motor, along with windings details of the stepper motor. Connect Q0 through Q3 outputs of IC4 in the control unit (Fig. 1) to positive and ground power supply terminals of the driver unit (Fig. 2). The waveform drive pattern of shift outputs of IC4 is shown in the table.

When you direct torchlight on the LDR, the stepper motor runs in one direction to latch the door. If you again focus torchlight on the LDR, the stepper motor runs in reverse direction to open the latch.

![](https://github.com/Sankul2699/LIGHT-OPERATED-LOCK/blob/master/Images/latch%20connection.JPG)
latch stepper motor interface




 
## Repository Contents
- **Presentation** - (Power point presentation) Get to know more about the project
- **Schematics** - Contains  circuit diagrams implemented
- **Images** - Images of the circuit and simulation 
- **Report** - contains the report of the project( word document)
