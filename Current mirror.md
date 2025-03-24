### Current Mirror 
The current mirror is an analog circuit that senses the reference current and generates the copy or number of copies of the reference current, with the same characteristics. The replicated current is as stable as the reference current source. The replicated current could be the same as the reference current (Id = Iref),
![image](https://github.com/user-attachments/assets/84f45841-62e3-4ba4-a334-0636348bb04e)

##### Fig 1: Current mirror circuit.
The relation between the Id and Iref can be given by the following expression.

Id = ( (W/L)1 / (W/L)ref ) * Iref

By changing the W/L ratio of the two transistors, the current which is fraction or multiple of the reference current can be generated. The only thing which needs to be ensured is that, the MOSFET should operate in the saturation region.
####Simulation

##### Fig 2:Example oriblem shown in class
![image](https://github.com/user-attachments/assets/df435a79-882b-428d-a4e3-36819b6412eb)
- Observation table for Iref=100u

##### PMOS CURRENT MIRROR
![Image](https://github.com/user-attachments/assets/9da3e268-b690-4c47-8e49-fec7c97a8512)
##### Fig 3: PMOS Current mirror circuit
In a PMOS current mirror, the source terminals of both transistors are connected to the supply voltage Vdd. The relationship between ID1 and IREF remains the same as in other configurations. The key requirement is to ensure that both M2 and M3 operate in the saturation region. This can be expressed as the condition VSD1 ≥ VSG - |VTP|, where VTP represents the threshold voltage of the PMOS transistor.

#### Simulation 
#### 1) Current mirror circuit with 1:1 ratio
Design a current mirror circuit which has a gain of AV = -10V/V, power supply of Vdd = 1.8V, and power of P <= 1mW. Find reference current (Iref), output current (Id), and total current (Itotal). Perform DC and AC analysis for mirror ratio 1:1, 1:2. Vary length from 180nm -> 500nm -> 1µm and do the analysis.
1) with length as 180n
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
##### 2) with length as 500nm
#### DC Ananlysis
![image](https://github.com/user-attachments/assets/f64a80a7-4786-4999-99bf-0b1218b2585f)
##### Fig 9: Output of DC Analysis
#### Transient Ananlysis
![image](https://github.com/user-attachments/assets/f4d94e8a-9685-47f0-9b94-4c83b41d6f14)
##### Fig 10:Output of Transient Analysis
#### AC Analysis
![image](https://github.com/user-attachments/assets/a8f4d2d8-6fa7-48b2-9d69-dd4a77baff54)
##### Fig 11: Output of AC Ananlysis
Av=38.8366dB Frequency=11.818MHz
Bandwidth = (38.8366-3dB)=35.8366 , Frequency= 54.52644MHz
##### 3) with length as 1u
#### DC Ananlysis
![image](https://github.com/user-attachments/assets/8d6ce3e9-8462-4a80-96f4-8f2121979018)
##### Fig 12: Output of DC Analysis
#### Transient Analysis
![image](https://github.com/user-attachments/assets/65ac6a33-7123-40e3-aa45-97929cde7944)
##### Fig 13: Output of Transient Analysis
#### AC Analysis
![image](https://github.com/user-attachments/assets/3e3006d5-1031-4fab-9a17-e5f24ec736a3)
##### Fig 14: Output of AC Ananlysis
Av=38.521746dB Frequency=10MHz
Bandwidth=(38.521746-3dB) = 35.521746dB , Frequency=41.09976MHz
#### Current Mirror CIrcuit with 1:2 Ratio

##### 1) With length as 180nnm
#### DC Ananlysis
![image](https://github.com/user-attachments/assets/1119a53c-488f-4885-97a6-f60ba8f896a6)
##### Fig 15:Output of DC Analysis
#### Transient Ananlysis
![image](https://github.com/user-attachments/assets/a99562ab-7e0a-4fe0-8521-ed1228d7f348)
##### Fig 16:Output of Tansient Ananlysis
#### AC Ananlysis
![image](https://github.com/user-attachments/assets/1748a3e7-09f7-422f-8c15-1166af4698dc)
##### Fig 17: Output of AC Analysis
Av=29.781147dB Frequency=10MHz
Bandwidth=(29.781147dB-3dB) = 26.781147 , Frrequency=268.26MHz
##### 2) With length as 500nm
#### DC Analysis
![image](https://github.com/user-attachments/assets/b4314a22-119a-4881-8425-eafaaacff93b)
##### Fig 18: Output of DC Analysis
#### Transient Ananlysis
![image](https://github.com/user-attachments/assets/3423b70f-38a4-4286-aabf-d5ba49ab598e)
##### Fig 18: Output of Transient analysis
#### AC Analysis
![image](https://github.com/user-attachments/assets/78c753b5-1885-44ea-9d7d-9191075940b7)
##### Fig 19:Output of AC Analysis
Av=38.83132dB Frequency=11.97085MHz
Bandwidth=(38.83132-3dB)=35.83132 , Frequency=53.830MHz
##### 3) with length as 1u




#### PART B
##### Design the differential amplifier using the same design specification as experiment 3(differential amplifier). Perform DC, Transient, AC analysis for the given circuit.
##### Circuit Diagram
![image](https://github.com/user-attachments/assets/34055db0-dd1a-4790-b42f-2cb62a55a53b)
##### Fig :Circuit Diagram
For this circuit biased voltage is replaced by current mirror circuit, with Vdd = 3.3V
the current through the circuite should be 0.378mA, hence Iss should be of 0.757mA.
#### DC Analysis

##### Fig :Output of DC Ananlysis
 the Vp and Vout values which is not exactly same as previous experiment, but nearer to that, this variation leads to change in gain of the circuit
##### Transient Analysis
![Image](https://github.com/user-attachments/assets/a0f30eb4-db54-4e19-8788-4ce31e6aa56a)
##### output of Tansient Analysis
#### AC Analysis
![image](https://github.com/user-attachments/assets/63e07c14-4cf3-4b08-8ac8-24ab4856877f)
##### Output of AC Analysis





