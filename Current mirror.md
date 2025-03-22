### Current Mirror 
The current mirror is an analog circuit that senses the reference current and generates the copy or number of copies of the reference current, with the same characteristics. The replicated current is as stable as the reference current source. The replicated current could be the same as the reference current (Id = Iref),
![image](https://github.com/user-attachments/assets/84f45841-62e3-4ba4-a334-0636348bb04e)

##### Fig 1: Current mirror circuit.
The relation between the Id and Iref can be given by the following expression.

Id = ( (W/L)1 / (W/L)ref ) * Iref

By changing the W/L ratio of the two transistors, the current which is fraction or multiple of the reference current can be generated. The only thing which needs to be ensured is that, the MOSFET should operate in the saturation region.
####Simulation

##### Fig 2:Example oriblem shown in class
![Image](https://github.com/user-attachments/assets/6f115bf6-af01-4e42-8027-3de811c5a76f)
- Observation table for Iref=100u

##### PMOS CURRENT MIRROR
![Image](https://github.com/user-attachments/assets/9da3e268-b690-4c47-8e49-fec7c97a8512)
##### Fig 3: PMOS Current mirror circuit
In a PMOS current mirror, the source terminals of both transistors are connected to the supply voltage Vdd. The relationship between ID1 and IREF remains the same as in other configurations. The key requirement is to ensure that both M2 and M3 operate in the saturation region. This can be expressed as the condition VSD1 ≥ VSG - |VTP|, where VTP represents the threshold voltage of the PMOS transistor.

#### Simulation 

Design a current mirror circuit which has a gain of AV = -10V/V, power supply of Vdd = 1.8V, and power of P <= 1mW. Find reference current (Iref), output current (Id), and total current (Itotal). Perform DC and AC analysis for mirror ratio 1:1, 1:2. Vary length from 180nm -> 500nm -> 1µm and do the analysis.
- 1 with length as 180n
![image](https://github.com/user-attachments/assets/ec823f17-66d5-4b5b-8f5f-650cb814ca37)
##### Fig 4:Circuit Diagram
Itotal = ( Power / Vdd )
= ( 1m / 1.8 )
= 0.55mA

Iref = Id = ( Itotal / 2 )
= 0.55m / 2
= 0.277mA
#### DC Ananlysis
![image](https://github.com/user-attachments/assets/66dbaded-8ed4-4f99-b83e-5dc9da33ad1b)
##### Fig 5: output of DC Ananlysis

##### Fig 6 : Tabular column of the analysis

#### Transient Analysis
![image](https://github.com/user-attachments/assets/2ee3938c-dbe8-4c71-81b1-ef285ec5567e)
##### Fig 7: Output of Transient Analysis

#### AC Analysis
![image](https://github.com/user-attachments/assets/a08667d9-8f63-4a35-ace9-04cbaff65b08)
##### Fig 8: Output of AC Ananlysis
AV=29.8364dB Frequency=10MHz
Bandwidth = (29.836dB-3dB) = 26.836dB , Frequency=278.8126MHz




