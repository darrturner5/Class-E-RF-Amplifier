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



