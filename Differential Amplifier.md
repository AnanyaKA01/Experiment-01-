### Differential Amplifier
The differential-pair or differential-amplifier setup is a fundamental and widely employed component in analog integrated-circuit design. 
It consists of two transistors, M1 and M2, whose sources are connected together. When the two transistors are subjected to different input voltages,
the currents through M1 and M2 will vary due to the gate voltages applied. However, if the gate voltages are equal, the currents through M1 and M2 will be the same
(Im1 = Im2). This configuration is referred to as a "Common-Mode Input Voltage Differential Amplifier." Regardless of the load resistor value,
it is crucial that the MOSFETs M1 and M2 do not enter the Triode region. It must be ensured that both MOSFETs remain in the Saturation Region.

![Image](https://github.com/user-attachments/assets/83747046-5ec2-4568-b42a-1288e7ed3cdc)
##### Fig 1 : Differential amplifier image

This Experiement is done in 3 stages.Where common source terminal is connected with

1.Resistor

2.Current source

3.MOSFET

For all this circuit we need find out the AC analysis ,Transient analysis And Frequency Response.
##### The given question specification is as follows
P=2.5mA ,VDD=3.3V ,Vin=1.65V ,Vocm=1.7V ,Vp=0.5V
- Iss=Id1=Id2=2.5/3.3=0.75mA
- RD=VDD-Vocm/Iss= 3.3-1.7/0.37=4.32KΩ
- Rss=Vp/Iss=0.5/0.75=666.6Ω
- By this value circuit is been built with respective to the values derived.
(Note:This value may change while getting the desired values in the saturation wise or some constant terms needs to set
### 1.Circuit 1 (Common Source terminal is connected to resistor):

In this circuit we have two MOSFET connected to same voltage input forming differential pair.
And Load Resistor is coonected to the Drain terminal of MOSFET. Source terminal is connected resistor and another 
terminal is connected to ground this is called source degenration resistor.
CIRCUIT:
![Image](https://github.com/user-attachments/assets/51db418b-9a1a-496f-9da9-6a8e24c98674)
The resistor applied at the common source terminal leads to change in the voltage gain ,input impedence in the circuit and the lineraity.
So the linearity increases and the impedence. As this is closed loop amplifier this leads to causes a feedbakback amplifier for all elements 
connecting to the common source terminal.
### DC analysis:
To do circit analysis first we need to check that the Both the MOSFET should be in the Saturation Region 
which should satisfy this.
VDS > VGS - Vth
![Image](https://github.com/user-attachments/assets/5fd9eaae-c8b2-4cf1-acb3-d1288e8e55c8)
#####Fig 2: Output of Dc Analysis
Transient Analysis:
The transient analysis explain the circuit response at a particular instant of time when a time-varying signal is applied at the inputs.
In this experiment we can see a complete phase shift of 180 degree output to the input signal.
As with respect to context of voltage gain, as the volatge gain is more leads to the smaller the bandwidth size.
At the particular time output wave changes with respect input in the amplitude.
![Image](https://github.com/user-attachments/assets/33280dc6-ab1f-4715-ada1-52216e2da62d)
##### Fig 3: Output of Transient analysis
Voltage Gain of this circuit is given by= Vout-Vin
Av=1.77-1.63/1.69-1.600=1.5
Therefore Higher the Higher resistor value reduces gain but increases bandwidth and more the transient response.
### AC Analysis:
Frequency response is determining quantity of bandwidth and stability of a MOSFET. This is divide into three regions;

1.Low frequency

2.Mid-band Frequency

3.High Frequency
In this experiment we can observe that there is no low frequency region because of there is no bypass or coupling capacitor in the circuit.
We can observe that mid band region upper value is nearear to the 3dB value which can used as
parameter to check bandwidth of amplifier to maintain its gain.
![Image](https://github.com/user-attachments/assets/da279294-984e-427a-84b9-7ed640f96eae)
##### Fig 4: Output of Ac Ananlysis
Gain =20log(Av) =20log(1.5) =3.5dB

### 2.Circuit 2 (Common Source terminal is connected to current source):
Same as the ciruit in the resistor circuit we need to replace resistor by current source .
We have two MOSFET connected to same voltage input forming differential pair.And current source is connected to the Drain terminal of MOSFET.
Source terminal is connected to the current source and another terminal is connected to ground.
![Image](https://github.com/user-attachments/assets/55eb1681-5ef1-450a-9c69-d401e7bf3a3f)
##### Fig 5:Circuit diagram with current source
### DC Analysis:
We need set voltage of Vicm to maintain the desired value of the current and voltage at source point.As a result opertaing point will be given as.
![Image](https://github.com/user-attachments/assets/e3c7427e-0e84-4e5c-b7bc-20c216176c97)
##### Fig 6: output od Dc Analysis
In the operating values we got the current flowing through the common source terminal is approximately what we had derived
in intial stage of the experiment.
### Transient Analysis:
The volatge gain of the ciruits inceases because of the current source drop across it is less compared to the 
Rs resistor drop. So the Voltage gain of circuit is more compared to the circuit 1
![Image](https://github.com/user-attachments/assets/8e7bbeea-d792-41a6-8156-32f8d604099e)
##### Fig 7:Output od transient analysis.
Voltage gain= vout/vin

          =(1.52-1.836)/(1.69-1.60)=3.511
          =3.511
### AC Analysis:
![Image](https://github.com/user-attachments/assets/5a157659-7d09-4494-932f-7e67d4bf2df4)
Gain in dB=20log(Av)
=20log(3.511)
=10.88
### 3. Circuit 3-(Connecting MOSFET to source terminal)
Now we are replacing the current source to the mosfet(M3) where we need to keep current Id3 as our desired value And to keep the mosfet(M1,M2,M3) in saturation region
so that voltage gain will be maintained.In this ciruit MMOsfet is connected to drain of it to source terminal and to other ground.
Now replace the current source with a Mosfet :
- Given vp=054v and wkt vt=0.36v
-  we got the gate voltage of the new mosfet as 0.866v
![Image](https://github.com/user-attachments/assets/48fc0ecc-2e1d-40b4-8823-921cf3790929)
###DC Analysis:
![Image](https://github.com/user-attachments/assets/2695bc6d-8040-4cd7-b799-36e7ae531a80)
#### Fig 9:output of Dc Ananlysis
By identifying the value of VB of MOSFET M3 we need check the current flow through the MOSFET and It should be in saturation region.

VB value (Gate terminal of MOSFET M3)=0.86v
The value of (W/L) in MOSFET 1&2 =180n/6.2u
The value of (W/L) in MOSFET 3  =180/19.5u

### Transient Anlysis:
![Image](https://github.com/user-attachments/assets/7d5e2f17-cb81-41de-a043-883405140f38)
##### Fig 10:Output of transient Ananlysis
Voltage gain(Av) = vout/vin =1.76-1.65/1.69-1.60=1.222
Av=1.721

### 4.Circuit-4
Here we are replacing Rd with diode connected PMOS which acts as resistor .
### DC Analysis
![Image](https://github.com/user-attachments/assets/abfebdce-7e48-40ba-8458-c93cf28b81c2)
##### Fig 11:Output of DC Analysis

### Transient Analysis
![Image](https://github.com/user-attachments/assets/87e15296-2f68-4bdd-aebd-e15bd5aba346)
##### Fig 12: output od Tansient ananlysis
Av=Vout/Vin = (1.65-1.71)/(1.69-1.60)
            = 0.6
Av in dB= 20log(0.6)=  4.436
### AC Analysis

### INFERENCE:
In this experiment, we seen the working principles of a differential amplifier and its types and configuration.

There are three types of configurations were implemented: resistor , current source , and an NMOS . All the implements work on different ways that results into the change in Voltage gain and stabillity of a mosfet.
-Resistor connection results in low CMRR and lower gain voltage, but offers high bandwidth and provides negative feedback.
-Current source connection improves CMRR and gain voltage, but slightly reduces bandwidth compared to a resistor.
-Resistor allows more common-mode signals to pass through, leading to lower rejection of noise.
-Current source offers better control of current, improving gain and common-mode rejection.
1.Need more Band width-Use Resistor configuration

2.Need more Gain-Use CMOSN Configuration

3.Need precise CMRR-Use current or CMOSN configuration
