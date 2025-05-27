# Telescopic Cascode Single-Ended Operational Transconductance Amplifier: Design and Performance Analysis

**Authors:**  

  
Ananya K A – Dept. of Electronics and Communication Engineering, The National Institute of Engineering, Mysore, India  
Email: 2023me_ananyaka_a@nie.ac.in 

MD Reyan – Dept. of Electronics and Communication Engineering, The National Institute of Engineering, Mysore, India  
Email: 2023me_mdreyan_a@nie.ac.in


---

## 1. Abstract

The telescopic cascode operational transconductance amplifier (OTA) is a high-performance analog circuit designed for high-frequency applications, offering superior gain and bandwidth. Its vertically stacked transistor configuration enhances output impedance while minimizing internal node capacitances, enabling low-noise and high-speed operation. This paper presents the design, technical specifications, advantages, and limitations of a telescopic cascode OTA implemented in TSMC 180nm CMOS technology. The topology achieves a gain of 60–80 dB and operates with a supply voltage of 1.8–2.5 V, making it suitable for applications such as pipeline ADCs, RF front-ends, and low-noise amplifiers. Despite its high gain and power efficiency, the design faces challenges with limited output swing and complex biasing requirements. This report evaluates the trade-offs and highlights the OTA’s suitability for precision analog signal processing.

---

## 2. Introduction

The telescopic Cascode operational transconductance amplifier (OTA) is a specialized analog circuit topology optimized for high-frequency and high-gain applications. By employing a vertically stacked configuration of NMOS and PMOS transistors, it combines a differential input pair with cascode transistors to achieve high output impedance and enhanced bandwidth. This architecture minimizes internal node capacitances, enabling superior high-frequency performance compared to conventional OTA designs. Its low-noise characteristics make it ideal for precision systems, including RF front-ends, data converters, and high-speed signal processing circuits.

This paper explores the design and performance of a telescopic cascode OTA implemented in TSMC 180nm CMOS technology. The following sections discuss the theoretical background, technical specifications, circuit advantages and disadvantages, and potential applications.

---

## 3. Theoretical Background

The telescopic cascode OTA derives its name from its unique structure, where cascode transistors are stacked in series with the differential pair, forming a linear alignment between power supplies. This configuration ensures that signal variations are handled by the fastest-polarity transistors, optimizing performance in high-gain applications. The primary design goal is to achieve high voltage gain, low noise, and minimal current consumption, with output swing as a secondary consideration.

To maintain transistor operation in the saturation region, a high-swing design is critical. The telescopic cascode architecture simplifies the signal path by using fewer current legs and components, sacrificing flexibility in output swing for reduced complexity. This makes it particularly suited for applications prioritizing speed and efficiency over wide dynamic range.

---

## 4. Technical Specifications

- **Technology:** TSMC 180nm CMOS
- **Software Used:** LTSpice

The bandwidth is influenced by the transconductance (gm) and load capacitance, while the high gain results from the cascode structure’s elevated output impedance.

---

## 5. Circuit Diagram

*(Insert Circuit Diagram Here in Repository)*

---

## 6. Working Principle

A telescopic operational transconductance amplifier (OTA) is a high-gain analog amplifier topology commonly used in integrated circuits. Its working principle involves stacking transistors in a vertical configuration, resembling the sections of a telescope, to maximize the output resistance and thus achieve high voltage gain. The input differential pair converts the input voltage into a current, which is then mirrored and passed through cascode transistors that boost the output impedance. This structure allows the OTA to operate with low power and high speed due to fewer internal nodes and minimal parasitic capacitance. However, the telescopic OTA has a limited output voltage swing, as the stacked transistors require significant voltage headroom to function properly. It is widely used in applications where high gain and efficiency are more critical than output range.

---

## 7. Simulation Results and Analysis

All the MOSFETs are in saturation region.

- **Power Dissipation:**  
  P = VI = 1.8 \times (2.3 \times 10^{-6}) = 4.14\mu W

| MOSFET Name | Length (nm) | Width (µm) |
|-------------|-------------|-------------|
| M0          | 180         | 0.8         |
| M1          | 180         | 0.5         |
| M2          | 180         | 0.5         |
| M3          | 180         | 0.3         |
| M4          | 180         | 0.3         |
| M5          | 180         | 0.6         |
| M6          | 180         | 0.6         |
| M7          | 180         | 0.5         |
| M8          | 180         | 0.5         |
| M10         | 180         | 2.0         |

### Transient Analysis

- Vout max = 1.92V  
- Vout min = 1.48V  

### AC Analysis

- Gain (Av) = 65.505 dB  

**Updated Results:**

- Vout max = 1.28V  
- Vout min = 1.20V  
- Gain (Av) = 59.816 dB ≈ 60 dB  

### Common Mode Analysis

- CMRR = ADM - ACM = 60 - (-25) = **85 dB**

---

## 8. Applications

1. ADCs (Pipeline, Sigma-Delta)  
2. Sample-and-Hold Circuits  
3. Switched-Capacitor Filters  
4. Analog Signal Processing  
5. PLLs and VCOs  
6. Low-Noise Amplifiers (LNAs)  
7. Precision Amplifiers  

---

## 9. Result Summary

| Parameter         | Specification   | Result       |
|------------------|------------------|--------------|
| Technology        | TSMC 180nm CMOS | TSMC 180nm CMOS |
| Supply Voltage    | 1.8V – 2.5V      | 1.8V         |
| Bandwidth         | Depends on capacitor value | 8.58 kHz   |
| Load Capacitance  | 1pF              | 1pF          |
| Gain              | 60–80 dB         | 60 dB        |
| CMRR              | Ideal (∞)        | 85 dB        |

---

## 10. Conclusion

The telescopic operational transconductance amplifier (OTA) demonstrates high performance in terms of voltage gain, bandwidth, and power efficiency, making it well-suited for high-speed and low-noise applications such as pipeline ADCs, RF front-ends, and precision biomedical systems. Its stacked transistor architecture enables a high gain in the range of 60–80 dB and excellent common-mode rejection (ideal or up to 85 dB), particularly when implemented in a 180nm CMOS technology. However, this same architecture introduces limitations in output voltage swing, requiring careful design and precise biasing, especially in low-voltage environments. Overall, the telescopic OTA proves to be an optimal choice for analog signal-processing applications that prioritize gain, speed, and noise performance over wide dynamic range.

---

## 11. References

1. Gaurav V. Bhawde et al., “Design, Fabrication and Analysis of Automatic Telescopic Mount”, 2018  
2. P. Tsela et al., “Thermal Analysis of the LLR Optical Telescope Tube Assembly”, 2016  
3. Naveen Withanage et al., “Designing and Testing of an OTA for Reflector Telescopes”
