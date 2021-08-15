# Whistler-Wave-Amplifier

- Whistler waves, also known as Very Low Frequency (VLF) waves fall under the frequency range of 3-30 kHz. 
- They have characteristically low attenuation rates and are particularly used in communication by military forces worldwide. The waves travel in a zigzag path around the Earth, reflected alternately by the Earth and the ionosphere, in TM (transverse magnetic) mode.
- A major practical drawback to this band is that because of the length of the waves, full-size resonant antennas (half-wave dipole or quarter-wave monopole antennas) cannot be built because of their physical height. 
- Vertical antennas must be used because VLF waves propagate in vertical polarization, but a quarter-wave vertical antenna at 30 kHz would be 2.5 kilometres (8,200 feet) high. To counter these effects, efficient amplification is necessary to ensure proper propagation and to reduce antenna size.

The entire circuit was designed and simulated on the LT Spice software.

The ciruit mainly consists of 3 secrions:

1. **Twin-T Notch Filter:** 
Notch filters are a highly selective, high-Q, form of the band stop filter which can be used to reject a single or very small band of frequencies rather than a whole bandwidth of different frequencies.

**Tuning the Twin-T Notch Filter:**

The Twin-T Notch Filter must be tuned to remove the external noise created by the AC Mains Hum. This can be done by choosing appropriate Resistance and Capacitance Values.
R = 11MΩ, C = 120pF

fN = 1/(4πRC) = 60.28 Hz ~ 60 Hz

2. **Low Pass Filter:** 
A Low Pass Filter is a circuit that can be designed to modify, reshape or reject all unwanted high frequencies of an electrical signal and accept or pass only those signals wanted by the user.

**Tuning the Low Pass Filter:**
The Low Pass Filter must be tuned to allow only the VLF waves to pass through and filter out the High Frequency Waves.
R1 = 150kΩ, R2 = 150kΩ, C1 = 25pF, C2 = 15pF

fC = 1/2π√𝑅1∗𝐶1∗𝑅2∗𝐶2 = 54.791kHz

f3dB = fC*√2^(1/n)−1 = 35.263 kHz

3. **Amplification:**
The amplification is done using a U309 JFET. This particular JFET was chosen because of its high sensitivity, high input impedance and low output noise. All factors favourable for low-frequency signal amplification.

Block Diagram:

![image](https://user-images.githubusercontent.com/69978515/129464257-7ae0e39d-fee2-4e9a-b124-2f1e27220524.png)

NOTE: For further details on the technical aspects of the project, kindly refer to the Ciruit diagram and simulation results.

