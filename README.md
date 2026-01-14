
---

## Technical Overview

### Common-Emitter Amplifier
- **Bias current:** 10 mA  
- **Transistor:** 2N2222 / 2N3904  
- **Midband gain:** ≈ −188 V/V  
- **Dominant limitation:** Miller-multiplied base–collector capacitance  

**Upper cutoff frequency**
- Hand analysis: ≈ **600 kHz**
- LTspice simulation: ≈ **740 kHz**
- Measurement: ≈ **540 kHz**
  
<img width="2556" height="1251" alt="ce_bode_magnitude" src="https://github.com/user-attachments/assets/679047e6-da4f-44d4-abbd-5b7497bdd1d5" />


This confirms that **Miller effect dominates the high-frequency response** of the CE stage.

---

### Cascode Amplifier
- CE input stage with **near-unity gain**
- Common-base output stage providing high voltage gain
- Suppresses Miller multiplication by **isolating the collector swing**

**Upper cutoff frequency**
- Hand analysis: ≈ **480 MHz**
- LTspice simulation: ≈ **440 MHz**
- Measurement: ≈ **1.2 MHz**
  
<img width="2556" height="1251" alt="cascode-ce-bode-plot" src="https://github.com/user-attachments/assets/2a366e8f-3224-4267-a1be-b9bb118cc2e4" />



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

