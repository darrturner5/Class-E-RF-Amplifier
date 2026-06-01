# Class-E-RF-Amplifier
Goal: Build a 12V, 15W, 250kHz Class E RF Amplifier.

I want to understand and see the effects of an RF Amplifier.

Tools:
- Falstad Circuit Simulator
- https://people.physics.anu.edu.au/~dxt103/160m/class_E_amplifier_design.pdf - Nathan Sokal design equations
- ARRL Handbook For Radio Communications 2024

Designed circuit components:
- RF Choke: 35.3 uH ( Air Core Inductor)
- IRLZ44N MOSFET + 400pf Drain Capacitance
- Shunt Capacitor: 20.7nF
- Phase Shifting Inductor: 4.1uH (Air Core Inductor)
- Series tuned capacitor: 29.9nF
- Series tuned inductor: 17.63uH (Air Core Inductor)
- Resistive load 5.5 ohms

<img width="2110" height="1568" alt="IMG_8824" src="https://github.com/user-attachments/assets/ddc0c451-c61d-4a3a-b30e-ccfc60f8407f" />
<img width="1576" height="2100" alt="IMG_8819" src="https://github.com/user-attachments/assets/0b097080-7252-46be-bf6c-f6c4b700973e" />
<img width="1576" height="2100" alt="IMG_8820" src="https://github.com/user-attachments/assets/03e96e5c-960b-459f-8915-e3f80085e1c3" />
<img width="1576" height="2100" alt="IMG_8821" src="https://github.com/user-attachments/assets/8e3c8832-5137-4447-b72a-53b5f6fb972d" />


For my air core inductors, I took the formula from the ARRL Handbook for Radio Communications which solved for inductance, given the diameter, number of turns and the inductor length.

I rearranged the formula for the number of turns since I already have a set inductance of 250kHz and can choose my inductor diameter and inductor length.
  
<img width="1551" height="1317" alt="IMG_8823" src="https://github.com/user-attachments/assets/cbfb83b7-b7eb-4c65-9762-b2728f76ee51" />


In Falstad Circuit Simulator, I can see the circuit in first hand and fine tune it.


<img width="800" height="521" alt="image" src="https://github.com/user-attachments/assets/d094dbe6-02ef-4198-bfe1-80ce9430ac57" />

- Drain Voltage is 47V
- When the MOSFET turns on it is really close to zero but not fully zero 300mV - 1.5V range 
- Power rating across the 5.5 Resistor load is around 13W when MOSFET turns off
- As the MOSFET turns linear, drain to source current peaks to about 2A while voltage is near zero.
- As the MOSFET turns off, drain to source voltage peaks to 47V while current is near zero.
- VDS seems to be rising as current approaches zero. (Power Dissipation)


*VIDEO BELOW:*

[![CLASS E RF AMPLIFIER SIMULATION](https://img.youtube.com/vi/REJCsYbso4U/0.jpg)](https://www.youtube.com/watch?v=REJCsYbso4U)




# Simulation Notes
*While the 5.5 ohm resistor load is ideal for the circuit, I dont have a 5.5 ohm load, instead Ill get a 5ohm power resistor and use it for the load.*

- 5 OHM LOAD:
- 45V Drain voltage max
- 150mV - 1.6V Drain voltage when MOSFET is on
- Drain Voltage rises slightly as current is falling (Power Dissipation)
- Peak output power around 12.8W
- IDS (Current Drain to Source) still peaks around 2A
- Input current 80mA - 891mA






