# Experiment-01
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
- power = 100uW
- We know that P=VI , where V=1.8V here
- Therefore, I = 55.5uA
- From loop equation : VDD = IDRD + Vout
- where VDD= 1.8,  ID=55.5uA,  RD=1KHz
- Therefore Vout= 1.745V
- Hence Q point= (1.745V, 55.5uA)

## 7)	Theory And Simulation Setup
#### DC Analysis :
In DC analysis the goal is to establish the stable operationg point for the MOSFET, ensuring it remains in the saturation region for proper amplification.The MOSFET operates in the saturation region when drain-source voltage(VDS) is greater than the overdrive voltage (VOV=VGS-VTH). the drain current is given by
ID= 1/2Kn(VOV)2
VDS and ID provides the operating point of the MOSFET.

### Tabular column
![Image](https://github.com/user-attachments/assets/85e0fbb1-84bb-46f4-807d-8e9b290f957c)

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
- Gain = 2 dB
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
      
![Image](https://github.com/user-attachments/assets/6ebcd342-313a-4876-bb7c-1cee2390556f)
##### Fig 8: Circuit with all the components

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
- power = 100uW
- We know that P=VI , where V=1.8V here
- Therefore, I = 55.5uA
- From loop equation : VDD = IDRD + Vout
- where VDD= 1.8,  ID=55.5uA,  RD=1KHz
- Therefore Vout= 0.864V
- Hence Q point= (0.864V, 55.5uA)

## 7)	Theory And Simulation Setup
#### DC Analysis :
In DC analysis the goal is to establish the stable operationg point for the MOSFET, ensuring it remains in the saturation region for proper amplification.The MOSFET operates in the saturation region when drain-source voltage(VDS) is greater than the overdrive voltage (VOV=VGS-VTH). the drain current is given by
ID= 1/2Kn(VOV)2
VDS and ID provides the operating point of the MOSFET.

![Image](https://github.com/user-attachments/assets/98d77580-ff6d-47e9-975b-0e7ea2f6c112)

##### Fig 9 : output of DC Ananlysis and Circuit

#### Transient analysis :
Transient analysis examines how the amplifier responds to time varying signals, such as pulse inputs or sudden changes in voltage. The behaviour is influenced by the charging and discharging of capacitors including coupling capacitors and bypass capacitors.The response of the amplifier due to the sudden changes in the input is limited by its time constants which depends upon the capacitance and resistance in the circuit. Transient analysis is crucial in high speed applications where rise time, fall time, propagation delay determines the amplifier's suitability for fast signals.

![Image](https://github.com/user-attachments/assets/c962a1dc-e3ae-4c30-a560-f90690fa08b7)
##### Fig 10 : Transient Analysis Parameters 

#### AC analysis:
In AC analysis MOSFET treated as a linear small-signal amplifier, where the drain current is proportional to small variations in gate volatge
iD=gmvgs
where gm is transconductance. Therefore, The voltage gain of the amplifier is given by
Av= -gm(RD||RL)
The negative sign indicates the 180 degree phase shift between the input and output signals. The input impedance is primarily determined by the gate biasing resitors whereas output impedance is largely influenced by the resistor RD . At low frequency the gain is effected by coupling capacitors and bypass capacitors, while at high frequencies by paracitic capacitors.

![Image](https://github.com/user-attachments/assets/5352346b-63c2-4fd6-bed8-ce41079212f7)
#### Fig 11 : AC Analysis Parameters

## 8)	Results 
#### 1. DC Analysis

![Image](https://github.com/user-attachments/assets/98d77580-ff6d-47e9-975b-0e7ea2f6c112)
##### Fig 12: DC Analysis Result

- ID = 55.5uA
- width(CMOSP) = 1107nm , L=180nm
- width(CMOSN) = 1107nm , L=180nm
- Vout = 0.864V
- DC operating point as (0.864V, 55.5uA)

   #### 2. AC Analysis
  
![Image](https://github.com/user-attachments/assets/a191bb8f-3413-4fdd-ada9-cd5cad36d288)
##### Fig 13 : AC Ananlysis Result
- The results shows that the circuit is not stable due to the poles and points .
- If we increase the value of W the value of ID is also increasing
-  Higher The value of W/L ratio leads to a wider bandwidth due to high transconductance
-  Lower thw Gain margin closer to the stability
-  The gain(5.5 dB) and phase shift (which is nearly 180deg) align with theoretical expectations.
   
#### 3. Tansient Ananlysis 

![Image](https://github.com/user-attachments/assets/78500041-f782-409f-8438-d06998c4f469)
##### Fig 14 : Transient Analysis Result

- The input waveform (Vin) is a sinusoidal signal centered at 0.7V
- The output waveform (Vout) is also sinusoidal but inverted, confirming the inverting nature of the common source amplifier.
- A common source amplifier typically provides a 180° phase shift between input (Vin) and output (Vout) at mid-frequency
- This phase shift deviates from ideal 180° due to the influence of parasitic capacitances, load resistance, and MOSFET characteristics.
- Vout= 1.660 for width of 878nm.

  #### VTC Curve

 ![Image](https://github.com/user-attachments/assets/2a0c6595-99ba-485f-9c59-84e1279532fc) 
##### Fig 15: vtc curve graph

- Graph Analysis:
- X-axis (Input Voltage, Vin): 0V to 1.8V
- Y-axis (Output Voltage, Vout): 1.8V to nearly 0V
- Threshold Voltage (Vth): The MOSFET starts switching at approximately 0.9V - 1.2V.
- Saturation Region: Beyond Vin ≈ 1.2V, the output voltage drops significantly.
- Cutoff Region: For Vin < 0.9V, the MOSFET is OFF, and Vout remains at 1.8V (Vdd).

## Inference
 - From the DC analysis, we determine the DC operating point of the MOSFET, which helps verify whether the transistor is functioning in the saturation region. This confirmation is crucial, as operation in saturation ensures that the MOSFET acts as an amplifier with the desired characteristics.
 - From the AC Analysis, As frequency increases, the gain begins to decrease due to the impact of MOSFET parasitic capacitances.The amplifier maintains a relatively constant gain in the low-frequency region, ensuring steady signal amplification within this range,The phase response gradually shifts with increasing frequency, approaching -180°, which is a characteristic of a common source amplifie.
- From the transient analysis, The transient response graph confirms that the circuit transitions smoothly over time.
The circuit responds effectively to input variations, indicating stable operation.

## Comparison Between Circuit 01 and Circuit 02
   
![Image](https://github.com/user-attachments/assets/934ce300-79ea-45ad-8328-4f333ee42972)
##### Fig 16: comparison Table

## Observation 

- Circuit 2 has a larger NMOS width to compsate for the active load configuration.
- Circuit 2 has a positive gain meaning it is acting more like a buffer and a constant current source due to active load , circuit 1 in contrast has a negative gain as expected in a common source configuration.
- Circuit 02 has a lower output voltage because the diode-co nnected PMOS introduc es a lower voltage drop compare d to a passive resistor.
- The larger W/L ratio in Circuit 02 helps improve current drive and transcon ductance in the presence of the PMOS load.
- difference in DC operating points is due to the voltage drop across the active load (PMOS diode) in Circuit 02, whereas Circuit 01 has a higher output voltage due to the resistor load.


