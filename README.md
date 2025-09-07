# Cell Phone Jammer Circuit - EEE 310 Project

## ⚠️ Legal Disclaimer
This project is for **educational and research purposes only**. RF jammers are illegal in most countries for civilian use. This was completed as part of university coursework at Bangladesh University of Engineering and Technology (BUET).

## Project Overview
A radio frequency signal jammer circuit designed to disrupt cellular communications within a limited range. The project successfully demonstrated jamming capabilities for FM radio frequencies around 100 MHz.

## 🎯 Objectives
- Design and implement a three-stage RF jammer circuit
- Understand RF signal disruption principles
- Demonstrate practical jamming at specific frequencies
- Analyze circuit limitations and improvements

## 🔧 Technical Specifications

### Circuit Components
- **Timer Stage**: NE555 IC configured as astable multivibrator
- **Amplifier Stage**: BF422 BJT in Class C configuration  
- **Tuning Stage**: LC tank circuit for frequency selection
- **Operating Frequency**: ~100 MHz (FM radio band)
- **Range**: Approximately 1 meter
- **Power Supply**: 9V DC

### Key Parameters
- Timer frequency: ~500 kHz
- Target frequency: 3877.3 MHz (theoretical)
- Achieved frequency: ~100 MHz (hardware limited)
- Amplifier efficiency: ~90% (Class C theoretical maximum)

## 🧪 Testing Results

### Simulation (PSPICE)
- Achieved periodic output around 100 MHz
- High-frequency envelope clearly visible
- Model parameters limited accuracy

### Practical Implementation
- Successfully jammed FM radio at 104.0 MHz and 106.0 MHz
- Clean audio became completely distorted when jammer active
- Effective range: ~1 meter with 24 AWG wire antenna

## 🚫 Limitations

1. **Hardware Constraints**: BJT frequency response limited to ~100 MHz
2. **Cellular Bands**: Modern phones operate at 698-806 MHz, 1920-1980 MHz, 2110-2170 MHz
3. **Range**: Limited by antenna design and power output
4. **Frequency Specificity**: Can only jam designed frequency range

## 🔮 Future Improvements

- Use RF transistors rated for GHz frequencies
- Implement better antenna design for increased range
- Include multiple frequency band coverage

## 👥 Team Members

**Group 06 - EEE 310, BUET**
- Md. Fahadul Islam (1906054)
- Tasmin Khan (1906055) 
- Bokhtiar Foysol Himon (1906056)
- Sayed Mommad Tawsif Arefin (1906057)

**Supervisors:**
- Dr. Mohammad Faisal (Professor)
- Mumtahina Islam Sukanya (Lecturer)

**Note:** This is a hardware design project - no traditional source code files are included.

## 🔗 References

1. Mobile Cell Phone Jammers Applications
2. Cellular Frequencies - Wikipedia  
3. RF Jammer Advantages and Disadvantages
4. ITU Radio Regulations for Bangladesh

---
*Completed: February 26, 2023 | BUET Department of Electrical and Electronics Engineering*
