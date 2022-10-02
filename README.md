Simple soft start circuit with power MOSFET and NTC.
It is designed to limit in-rush current of a DCDC converter connected to a battery with XT90i (like XT90 + 2 signal pins) connectors. 
The additional signal pin makes sure that the circuit resets after the connector is unplugged. Otherwise, it can be powered by the input capacitor of the load and doesn't "know" that the battery power is lost.
Because battery voltage changes with battery SoC, absolute voltage at load input cannot tell wether the input capacitance is fully charged.

The 78L15 is the power supply for MOSFET driving and is a reference voltage at the same time. Q2 protects the NTC from long current exposure if the connector is plugged in to slowly or not properly.
The comparator switches on once the voltage drop accross the NTC falls below the value defined by the potentiometer and R1,R2. With the given resistor values, the circuit works with battery voltage upto 60V.
Note that 78L15 max input is 30V.

You can omit and short Q2 if you dont use a seperate power supply for circuit.


NTCs
https://datasheetspdf.com/pdf/814993/EXSENSE/NTC-10D7/1


MOSFETS

* IPP024N08NF2SAKMA1 (80V, 2.4mohm, Id100 139A)
* IRF100B201 (100V, 4.2mohm, Id100 136A)