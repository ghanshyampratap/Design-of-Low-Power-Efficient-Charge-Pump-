# Design of Low Power & Efficient Charge Pump for Non-Volatile Memory Applications

##  Introduction

Non-volatile memories (NVMs) — such as **NAND Flash** and **EEPROM** — are fundamental components in SSDs, smartphones, USB drives, and embedded systems. These memories require **high voltage levels (10–20 V)** for program/erase operations, whereas the supply voltage is typically only **1.2–3.3 V**.  

A **charge pump** is an on-chip voltage multiplier that generates these high voltages without external components.  

### Key Challenges
- Low power consumption  
- High efficiency  
- Reduced ripple  
- Compact CMOS integration  

### Integration Advantage
Fully integrated CMOS charge pumps eliminate external high-voltage sources, making the system **more compact and cost-effective**.


## Problem Statement
Existing charge pump topologies face limitations:
- Poor efficiency metrics for regulated outputs  
- Low power only at low supply voltages  
- Limited output generation (~10 V)  
- High ripple and low peak efficiency (~49%)  
- Use of outdated 180 nm process technologies  

<img width="1184" height="665" alt="image" src="https://github.com/user-attachments/assets/46034b89-4f95-4b94-9ba5-75c5ee75bbd9" />





## Design Specifications

| Parameter | Value |
|------------|--------|
| Technology Node | 90 nm GPDK |
| Supply Voltage | 3.3 V |
| Output Voltage | 19 V |
| Power Consumption | ≤ 1.59 mW |
| Power Efficiency | ≥ 19.74 % |
| Output Ripple | ≤ 600 mV |
| Rise Transition | ≤ 1.785 µs |




## Project Objective

> **To design a charge pump that generates 19 V from a 3.3 V supply using Cadence Virtuoso with 90 nm GPDK.**





## Design Topologies Tested

1. **Dickson Charge Pump** – Simple, area-efficient, but suffers from threshold voltage (Vth) drop.  
2. **Cross-Coupled Charge Pump** – Cancels Vth drops for higher efficiency.  
3. **Charge Transfer Switch Pump** – Uses transmission gate-style switches for very low threshold loss.




## Simulation Results (90 nm)

| Metric | Observation | Improvement |
|---------|--------------|--------------|
| Power Consumption | Reduced by **92.85 %** | Fewer transistors and simpler ladder |
| Power Efficiency | Improved by **100.51 %** | Single ladder design |
| Rise Transition | Increased by **12.7 %** | Due to single ladder |
| Ripple | Reduced by **36.5 %** | Less switching and jitter |




<img width="1209" height="641" alt="image" src="https://github.com/user-attachments/assets/5733e5f9-a0f5-4e46-a93f-52e8d4ea6eae" />
<img width="1196" height="680" alt="image" src="https://github.com/user-attachments/assets/ec1d0ea8-a56a-4b64-bb27-a7a6c73e5992" />
<img width="1213" height="656" alt="image" src="https://github.com/user-attachments/assets/8d13447b-927d-465f-a3bd-ac87da411132" />
<img width="1208" height="689" alt="image" src="https://github.com/user-attachments/assets/d953ac38-daf6-4473-b0a7-c092a7f2ba41" />
<img width="1207" height="684" alt="image" src="https://github.com/user-attachments/assets/99aa5a08-e33a-4cff-b9c8-acb61b1cc30f" />




## Advantages

- Reduced ripple → reliable memory operation  
- Higher efficiency → energy saving in portable devices  
- Adaptive control → better performance under variable loads  
- Compact CMOS design → low-cost integration  

## Applications

- NAND Flash & EEPROM in SSDs, smartphones, and USB drives  
- Low-power embedded systems and IoT devices  
- On-chip power management ICs  
- High-voltage drivers for displays and RF systems  

<img width="1219" height="403" alt="image" src="https://github.com/user-attachments/assets/df5b32ee-f5db-483a-9bc2-32ad44cb06d6" />
<img width="1222" height="630" alt="image" src="https://github.com/user-attachments/assets/56d69fa5-4841-445c-b98c-621f8caf1508" />
<img width="1214" height="687" alt="image" src="https://github.com/user-attachments/assets/3aa6e71b-fc86-481c-8356-c71e96ed40d1" />


## Flow of the Project

1. Literature Review  
2. Circuit Design & Simulation  
3. Parameter Optimization  
4. Efficiency & Ripple Analysis  
5. Integration in NVM Systems  


## Conclusion

The proposed **low-power Dickson charge pump** in 90 nm technology achieves:
- Significant reduction in power consumption  
- Improved efficiency  
- Reduced ripple  
- Compact CMOS-compatible design  

This makes it ideal for **non-volatile memory (NVM)** and **low-power embedded applications**.

## Future Work

- Optimize **W/L ratios** for best performance in power, efficiency, rise time, and ripple  
- Analyze **body effect** impact on output voltage  
- Reduce the number of stages without compromising performance  
- Integrate the design in **NVM applications**

##  References

1. Jamuna, S. et al. (2025). *Design and Analysis of Multi-Level Voltage Generator for NAND Flash Operations Using a Reference Voltage Controlled Charge Pump.* Research Square Preprints, rs-6867812.  
2. Lin, Z. et al. (2025). *A Novel Multi-Mode Charge Pump in Word Line Driver for Compute-in-Memory Arrays.* Electronics, 14(2), 175.  
3. You, Y. et al. (2025). *A Multi-Phase Cross-Coupled Charge Pump for High-Side Switch Driver in Battery Protection System.* Microelectronics Journal, 166, 106900.  
4. Rahman, L. F. et al. (2021). *Design Topologies of a CMOS Charge Pump Circuit for Low Power Applications.* Electronics, 10(6), 676.  
5. Wang, Q. et al. (2018). *A 12 V Low-Ripple and High-Efficiency Charge Pump with Continuous Regulation Scheme for 3D NAND Flash Memories.* IEEE ICSIct.
