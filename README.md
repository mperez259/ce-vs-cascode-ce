
---

## Technical Overview
<img width="1846" height="1031" alt="image" src="https://github.com/user-attachments/assets/5f8dc7e1-7832-4db0-9acb-535317842357" />

### Common-Emitter Amplifier
- **Bias current:** 10 mA  
- **Transistor:** 2N2222 / 2N3904  
- **Midband gain:** ≈ −188 V/V  
- **Dominant limitation:** Miller-multiplied base–collector capacitance  

**Upper cutoff frequency**
- Hand analysis: ≈ **600 kHz**
- LTspice simulation: ≈ **740 kHz**
- Measurement: ≈ **540 kHz**

This confirms that **Miller effect dominates the high-frequency response** of the CE stage.

---

### Cascode Amplifier
- CE input stage with **near-unity gain**
- Common-base output stage providing high voltage gain
- Suppresses Miller multiplication by **isolating the collector swing**

**Upper cutoff frequency**
- Hand analysis: ≈ **4.8 MHz**
- LTspice simulation: ≈ **4.4 MHz**
- Measurement: ≈ **1.2 MHz**

Despite parasitic and device-level non-idealities, the cascode shows a **clear bandwidth improvement** over the CE amplifier.

---

## Key Concepts regarding high frequency behavior

- Miller effect and capacitance partitioning
- Dominant-pole frequency estimation
- Hybrid-π small-signal modeling
- Transition frequency (f<sub>T</sub>)–based capacitance extraction
- Practical vs ideal bandwidth discrepancies
- Why cascodes are foundational in **RF ICs and wideband analog design**

---

## Tools Used

- **LTspice** – AC sweep and frequency response analysis  
- **Oscilloscope & signal generator** – experimental validation  
- **Hand analysis** – small-signal and high-frequency modeling  

---

## Possible Extensions

- Replace BJTs with **MOSFET cascodes**
- Extract parasitics from datasheet corner cases
- Extend analysis to **noise and output impedance**
- Compare folded vs telescopic cascode topologies

---

