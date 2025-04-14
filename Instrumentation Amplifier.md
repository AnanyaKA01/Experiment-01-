## Instrumentation Amplifier
### What is an Instrumentational Amplifier?
-  An instrumentation amplifier (INA) is a very special type of differential input
amplifier; its primary focus is to provide differential gain and high common-mode
rejection.
-  INAs offer high input impedance and low output impedance; newer devices will
also offer low offset and low noise.


![image](https://github.com/user-attachments/assets/29e15ec6-9375-4526-b207-01c1cddb0da6)
##### Fig 1: Circuit Diagram of Instrumenatational Amplifier
### Question Given : Design an Instrumentation amplifier using 3 op-amp configuration with the following constraint
### a)R1=R2=R3=R4=R5=R6=100KΩ
### b) Difference gain Adm=20V/V - Find Acm and calculate CMRR for Adm=20V/V and 50V/V , Use LTspice Simulator.


#### 1) For Adm = 20V/V
![image](https://github.com/user-attachments/assets/0e66fd33-ee12-43fd-8da6-1904752859b5)
##### Fig 2: Circuit Diagram
- ADM = (R2 / R1) × [1 + 2 × (R5 / RG)]
- 20 = (100k / 100k) × [1 + 2 × (100k / RG)]
- RG = 10.52KΩ

#### Transient Analysis for Adm
![image](https://github.com/user-attachments/assets/b67244ba-2e5d-4ec9-b21c-2724c495a357)
##### Fig 3: Ananlysis of Adm.
11.99/2-1.4 = 19.9833 ≈ 20.
#### Transient Analysis for Acm
![image](https://github.com/user-attachments/assets/48b59278-7414-4b9a-bc56-4439808f7d9a)
##### Fig 4: Analysis of Acm
- (47.48×10^-9)-(47.48×10^-9) / 0.5+0.5
- = 9.496×10^-8.

CMRR = Adm/Acm = 20V/V / 9.496×10^-8
      = 210614 = 20log(210614) = 166.4697dB.
      
#### 2) For Adm = 50V/V

- ADM = (R2 / R1) × [1 + 2 × (R5 / RG)]
- 50 = (100k / 100k) × [1 + 2 × (100k / RG)]
- RG = 4.081KΩ
#### Transient Ananlysis for Adm.
![image](https://github.com/user-attachments/assets/e2492aec-5502-468c-8def-f8d8ca841d4f)
##### Fig 5: Analysis of Adm
11.99/1-0.76 = 49.958 ≈ 50V/V.
#### Transient Ananlysis for Acm.
  ![image](https://github.com/user-attachments/assets/498a4d49-0109-4cda-8f28-1f4c9a66c8cc)
##### Fig 6: Analysis of Acm
- (47.48×10^-9)-(47.48×10^-9) / 0.5+0.5
- = 9.496×10^-8.
CMRR = Adm/Acm = 50V/V / 9.496×10^-8
= 5265374 = 20log(5265374) = 174.4285dB.

In order to take average of CMRR we are considering another 3 values for Adm and changing the value of RG Accordingly for realistic Performance assessment.

#### 3) For Adm = 80V/V
- ADM = (R2 / R1) × [1 + 2 × (R5 / RG)]
- 80 = (100k / 100k) × [1 + 2 × (100k / RG)]
- RG = 2.5316KΩ
#### Transient Ananlysis for Adm.
![image](https://github.com/user-attachments/assets/473729aa-43d0-4280-8fd5-3e4a0b7c3f47)
##### Fig 7: Analysis of Adm
11.99/2-1.850 = 79.9333 ≈ 80V/V.
#### Transient Ananlysis for Acm.
![image](https://github.com/user-attachments/assets/4117ad48-c07d-4493-b4a8-d72fc5a93a35)
##### Fig 8: Analysis of Acm
- (47.48×10^-9)-(47.48×10^-9) / 0.5+0.5
- = 9.496×10^-8.
CMRR = Adm/Acm = 80V/V / 9.496×10^-8
= 8424599 = 20log(8424599) = 178.5109 dB.

#### 4) For Adm = 120V/V
- ADM = (R2 / R1) × [1 + 2 × (R5 / RG)]
- 120 = (100k / 100k) × [1 + 2 × (100k / RG)]
- RG = 1.6807KΩ
#### Transient Ananlysis for Adm.
![image](https://github.com/user-attachments/assets/af19f6e5-9639-46cf-8df3-5de16f28a070)
##### Fig 9: Analysis of Adm
11.998/2-1.90 = 119.9  ≈ 120V/V.
#### Transient Ananlysis for Acm.
![image](https://github.com/user-attachments/assets/68064cb6-7213-45db-a03f-5c29b920be6b)
##### Fig 10: Analysis of Acm
- (47.48×10^-9)-(47.48×10^-9) / 0.5+0.5
- = 9.496×10^-8.
CMRR = Adm/Acm = 120V/V / 9.496×10^-8
= 12636899 =20log(12636899) = 182.032dB.

#### 5) For Adm = 150V/V
- ADM = (R2 / R1) × [1 + 2 × (R5 / RG)]
- 150 = (100k / 100k) × [1 + 2 × (100k / RG)]
- RG = 1.3423KΩ
#### Transient Ananlysis for Adm.
![image](https://github.com/user-attachments/assets/452b0d95-62a6-4be1-a3b9-a0b5116324f0)
##### Fig 11: Analysis of Adm
11.99/1-0.9200 = 149.875 ≈ 150V/V.
#### Transient Ananlysis for Acm.
![image](https://github.com/user-attachments/assets/e7244ff9-e9e7-413e-a67f-bc5377d6fddb)
- (47.48×10^-9)-(47.48×10^-9) / 0.5+0.5
- = 9.496×10^-8.
CMRR = Adm/Acm = 150V/V / 9.496×10^-8
= 1579612 = 20log(1579612) = 183.97dB.
