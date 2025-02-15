# Experiment-01-
## 1)	Title page
LT spice Simulation of Common source Amplifier

## 2)	Objective 
The objective of this report  is to use LTspice to examine a Common Source (CS) amplifier's performance utilizing DC, transient, and AC analysis. Determining the operating point (Q-point) and confirming biasing conditions are the goals of the DC analysis. Transient analysis is used to assess the dynamic behavior of the amplifier by monitoring its time-domain response to input signals. The frequency response, gain, bandwidth, and phase properties of the amplifier are ascertained using the AC analysis. To comprehend the amplifier's capabilities and constraints, the outcomes of these simulations will be contrasted with theoretical predictions.

## 3)	Circuit Description
•	Circuit Components
   - NMOS (180nm technology node)
   - Resistor- 1K
   - Voltage source (1.8V, 0.9V)
   - AC ground
   - Wries

## 4)	Circuit Schematic 

![Image](https://github.com/user-attachments/assets/ec8f8b75-d20b-43cb-8aa9-90088cc2317c)
##### Fig 1: CS Amplifier with all the components

## 5)	Procedure 
1.	Build the common source amplifier circuit as the circuit diagram using LTspice.
2.	Set the Resistor value as 1K, DC voltage as 1.8V, Gate voltage as 0.9V.
3.	Download the library file tsmc018 (1).txt
4.	Create a folder. Save the library file and LTspice file to the folder.
5.	Import the library file to LTspice using spice directive(.op).
6.	Set the mosfet model name CMOSN as given in the library file, length as 180nm, width as 1uF.
7.	Find the current value for the given power rating.
8.	DC analysis: In edit simulation option, change to dc offset to get list of values obtained from the circuit. We should get the calculated current value in the simulation result.So that we need vary the value of width since width is directly proportional to Drain current(Id) keeping other parameters constant.
9.	Transient analysis: In edit simulation option, change from dc offset to transient. Set the dc offset as 0.9V, Amplitude 50mV, frequency 1KHz. Keep stop time for 3ms and run to get the expected waveform.
10.	AC analysis : In edit simulation option, change from transient to ac analysis. Set type of sweep as decade, number of points per decade as 20, start and stop frequency as 0.1Hz and 1THz to get the expected ac waveform.

## 6)	Calculation
power = 100uW
We know that P=VI , where V=1.8V here
Therefore, I = 55.5uA
From loop equation : VDD = IDRD + Vout
where VDD= 1.8,  ID=55.5uA,  RD=1KHz
Therefore Vout= 1.745V
Hence Q point= (1.745V, 55.5uA)

## 7)	Theory And Simulation Setup
#### DC Analysis :
In DC analysis the goal is to establish the stable operationg point for the MOSFET, ensuring it remains in the saturation region for proper amplification.The MOSFET operates in the saturation region when drain-source voltage(VDS) is greater than the overdrive voltage (VOV=VGS-VTH). the drain current is given by
ID= 1/2Kn(VOV)2
VDS and ID provides the operating point of the MOSFET.

### Tabular column

![Image](https://github.com/user-attachments/assets/dbcd8a5b-7033-43c8-b5f2-beccfa3f596a)

![Image](https://github.com/user-attachments/assets/8081cf6c-e742-46bf-b9c3-7e5f98817674)
##### Fig 2 : output of DC Ananlysis and Circuit

#### Transient analysis :
Transient analysis examines how the amplifier responds to time varying signals, such as pulse inputs or sudden changes in voltage. The behaviour is influenced by the charging and discharging of capacitors including coupling capacitors and bypass capacitors.The response of the amplifier due to the sudden changes in the input is limited by its time constants which depends upon the capacitance and resistance in the circuit. Transient analysis is crucial in high speed applications where rise time, fall time, propagation delay determines the amplifier's suitability for fast signals.

![Image](https://github.com/user-attachments/assets/eaa14547-bd3c-4dd5-9cd0-f6df86f5e690)
##### Fig 3: Transient Analysis Parameters 

#### AC analysis:
In AC analysis MOSFET treated as a linear small-signal amplifier, where the drain current is proportional to small variations in gate volatge
iD=gmvgs
where gm is transconductance. Therefore, The voltage gain of the amplifier is given by
Av= -gm(RD||RL)
The negative sign indicates the 180 degree phase shift between the input and output signals. The input impedance is primarily determined by the gate biasing resitors whereas output impedance is largely influenced by the resistor RD . At low frequency the gain is effected by coupling capacitors and bypass capacitors, while at high frequencies by paracitic capacitors.

![Image](https://github.com/user-attachments/assets/f5d9c78f-45de-4b91-9eca-6d8c4d23b39b)
#### Fig 4: AC Analysis Parameters

## 8)	Results 
#### 1. DC Analysis

![Image](https://github.com/user-attachments/assets/8081cf6c-e742-46bf-b9c3-7e5f98817674)
##### Fig 5: DC Analysis Result

- ID = 55.5uA
- width = 0.203um
- Vout = 1.745V
- DC operating point as (1.745V, 55.5uA)

  #### 2. AC Analysis

  ![Image](https://github.com/user-attachments/assets/eb0725db-8f27-4adb-bbad-87b8fc9cc726)
##### Fig 6: AC Ananlysis Result

- At Frequency = 204.527 kHz
- Gain = -5.391 dB
- Phase shift = 128.261°
  
#### 3. Tansient Ananlysis 

![Image](https://github.com/user-attachments/assets/24d8bf03-48cb-4eea-878f-98e55c54f8a9)
##### Fig 7: Transient Analysis Result

- A common source amplifier typically provides a 180° phase shift between input (Vin) and output (Vout) at mid-frequency.
- From the ploted graph, the phase shift at 204.527 kHz (marked on the graph) is approximately 128.26°
- This phase shift deviates from ideal 180° due to the influence of parasitic capacitances, load resistance, and MOSFET characteristics.
- Vout= 1.745V for width of 0.203um

  ## Inference
 - From the DC analysis, we determine the DC operating point of the MOSFET, which helps verify whether the transistor is functioning in the saturation region. This confirmation is crucial, as operation in saturation ensures that the MOSFET acts as an amplifier with the desired characteristics. 

- From the Ac analysis, The gain drops at high frequencies due to the bandwidth limitation,As frequency increases, the phase shift gradually approaches negative values, indicating a typical low-pass filter behavior of the common source amplifier, the common source amplifier operates as a voltage amplifier with a limited high-frequency response due to intrinsic capacitances.

- From the Transient analysis, At low frequencies, the phase shift remains close to 180°, confirming the inverting nature of the amplifier,At higher frequencies, the phase shift decreases due to the effects of the parasitic capacitances


# CIRCUIT-02

## 1)	Circuit Description
   •	Circuit Components
   - NMOS (180nm technology node)
   - PMOS (180nm technology node)
   - Voltage source (1.8V, 0.7V)
   - AC Ground
   - Wires 
      
## 4)	Circuit Schematic     
      
![Image](https://github.com/user-attachments/assets/7ddf9bb3-750a-4fc9-98cc-76013eb6eff4)
##### Fig8: Circuit with all the components

## 5)	Procedure 
1.	Build the common source amplifier circuit as the circuit diagram using LTspice.
2.	Here the PMOS is diode connected and always remains in the saturation region such that it acts as a constant current source for the circuit.
3.	Download the library file tsmc018 (1).txt
4.	Create a folder. Save the library file and LTspice file to the folder.
5.	Import the library file to LTspice using spice directive(.op).
6.	Set the mosfet model name CMOSN and CMOSP as given in the library file.
7.	Find the current value for the given power rating.
8.	set the value of Width and Lenght according to value of current derived such that the aspect ratios are same and remains in saturation region.
9.	Do the DC sweep Analysis by giving the required parameters and generate the VTC curve for the circuit.
10.	DC analysis: In edit simulation option, change to dc offset to get list of values obtained from the circuit. We should get the calculated current value in the simulation result.So that we need vary the value of width since width is directly proportional to Drain current(Id) keeping other parameters constant.
Transient analysis: In edit simulation option, change from dc offset to transient. Set the dc offset as 0.7V, Amplitude 50mV, frequency 1KHz and AC Amplitude as 1. Keep stop time for 1ms and run to get the expected waveform.
AC analysis : In edit simulation option, change from transient to ac analysis. Set type of sweep as decade, number of points per decade as 20, start and stop frequency as 0.1Hz and 1THz to get the expected ac waveform.

## 6)	Calculation
power = 100uW
We know that P=VI , where V=1.8V here
Therefore, I = 55.5uA
From loop equation : VDD = IDRD + Vout
where VDD= 1.8,  ID=55.5uA,  RD=1KHz
Therefore Vout= 1.745V
Hence Q point= (1.745V, 55.5uA)

## 7)	Theory And Simulation Setup
#### DC Analysis :
In DC analysis the goal is to establish the stable operationg point for the MOSFET, ensuring it remains in the saturation region for proper amplification.The MOSFET operates in the saturation region when drain-source voltage(VDS) is greater than the overdrive voltage (VOV=VGS-VTH). the drain current is given by
ID= 1/2Kn(VOV)2
VDS and ID provides the operating point of the MOSFET.

![Image](https://github.com/user-attachments/assets/b519ebb3-3746-479b-b5e5-5898bad96bf6)
##### Fig 2 : output of DC Ananlysis and Circuit

#### Transient analysis :
Transient analysis examines how the amplifier responds to time varying signals, such as pulse inputs or sudden changes in voltage. The behaviour is influenced by the charging and discharging of capacitors including coupling capacitors and bypass capacitors.The response of the amplifier due to the sudden changes in the input is limited by its time constants which depends upon the capacitance and resistance in the circuit. Transient analysis is crucial in high speed applications where rise time, fall time, propagation delay determines the amplifier's suitability for fast signals.

![Image](https://github.com/user-attachments/assets/de6849b1-cd6a-4ddb-a06e-adf932ec9963)
##### Fig 3: Transient Analysis Parameters 

#### AC analysis:
In AC analysis MOSFET treated as a linear small-signal amplifier, where the drain current is proportional to small variations in gate volatge
iD=gmvgs
where gm is transconductance. Therefore, The voltage gain of the amplifier is given by
Av= -gm(RD||RL)
The negative sign indicates the 180 degree phase shift between the input and output signals. The input impedance is primarily determined by the gate biasing resitors whereas output impedance is largely influenced by the resistor RD . At low frequency the gain is effected by coupling capacitors and bypass capacitors, while at high frequencies by paracitic capacitors.

![Image](https://github.com/user-attachments/assets/f5d9c78f-45de-4b91-9eca-6d8c4d23b39b)
#### Fig 4: AC Analysis Parameters

## 8)	Results 
#### 1. DC Analysis

##### Fig 5: DC Analysis Result

- ID = 55.5uA
- width(CMOSP) = 878nm
- width(CMONP) = 878nm
- Vout = 1.660V
- DC operating point as (1.660V, 55.5uA)

   #### 2. AC Analysis


##### Fig 6: AC Ananlysis Result

- At Frequency = 204.527 kHz
- Gain = -5.391 dB
- Phase shift = 128.261°
