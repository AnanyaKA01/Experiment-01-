### Telescopic Cascode Single Ended Operational Transconductance Amplifier

#### 1.	Abstract
The telescopic cascode operational transconductance amplifier (OTA) is a high- performance analog circuit designed for high-frequency applications, offering superior gain and bandwidth. Its vertically stacked transistor configuration enhances output impedance while minimizing internal node capacitances, enabling low-noise and high-speed operation. This paper presents the design, technical specifications, advantages, and limitations of a telescopic cascode OTA implemented in TSMC 180nm CMOS technology. The topology achieves a gain of 60–80 dB and operates with a supply voltage of :      
1.8–2.5 V, making it suitable for applications such as pipeline ADCs, RF front-ends, and low-noise amplifiers. Despite its high gain and power efficiency, the design faces challenges with limited output swing and complex biasing requirements. This report evaluates the trade-offs and highlights the OTA’s suitability for precision analog signal processing.

#### 2.	Introduction
The telescopic Cascode operational transconductance amplifier (OTA) is a specialized analog circuit topology optimized for high-frequency and high-gain applications. By employing
a vertically stacked configuration of NMOS and PMOS transistors, it combines a differential input pair with cascode transistors to achieve high output impedance and enhanced bandwidth. This architecture minimizes internal node capacitances, enabling superior high-frequency performance compared to conventional OTA designs. Itslow-noise characteristics make it ideal for precision systems, including RF front-ends, data converters, and high-speed signal processing circuits.This paper explores the design and                  performance of a telescopic cascode OTA implemented in TSMC 180nm CMOS technology. The following sections discuss the theoretical background, technical specifications, circuit advantages and disadvantages, and potential applications.

#### 3.Theoretical Background
The telescopic cascode OTA derives its name from its unique structure, where cascode transistors are stacked in series with the differential pair, forming a linear alignment between power supplies . This configuration ensures that signal variations are handled by the fastest-polarity transistors, optimizing performance in high-gain applications. The primary design goal is to achieve high voltage gain, low noise, and minimal current consumption, with output swing as a secondary consideration.
To maintain transistor operation in the saturation region, a high-swing design is critical. The telescopic cascode architecture simplifies the signal path by using fewer current legs and components, sacrificing flexibility in output swing for reduced complexity. This makes it particularly suited for applications prioritizing speed and efficiency over wide dynamic range.

#### 4.Technical Specifications
     The OTA is designed using TSMC 180nm CMOS technology,	with key specifications outlined in Table. 
![Image](https://github.com/user-attachments/assets/f6a92495-5628-4871-b46e-0efbfbe410e0)
