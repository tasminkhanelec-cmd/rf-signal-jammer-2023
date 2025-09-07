# Design Equations and Theory

## NE555 Timer Design

### Astable Multivibrator Configuration

**Frequency Equation:**
```
f = 1.44 / ((R1 + 2R2) × C1)
```

**Period Calculation:**
```
T = 0.693 × (R1 + 2R2) × C1
```

**High Time:**
```
t_high = 0.693 × (R1 + R2) × C1
```

**Low Time:**
```
t_low = 0.693 × R2 × C1
```

**Duty Cycle:**
```
D = (R1 + R2) / (R1 + 2R2) × 100%
```

### Design Constraints
- **Frequency range**: 2-3 MHz maximum for NE555
- **Duty cycle**: Always > 50% due to circuit topology
- **Component ratios**: R1 >> R2 for lower duty cycles

## Class C Amplifier Design

### Conduction Angle
```
θ = 2 × arccos(Vbe + Vbias) / Vin_peak)
```

Where:
- **θ**: Conduction angle (80° - 120° typical)
- **Vbe**: Base-emitter voltage (~0.7V)
- **Vbias**: Reverse bias voltage (set by Rb)

### Efficiency Calculation
```
η = (Pout / Pin) × 100%
```

**Theoretical maximum efficiency for Class C:**
```
η_max ≈ 90%
```

### Bias Point Design
```
Vq = Vcc × R2 / (R1 + R2) - Vbe
```

Where Vq should be below cutoff for Class C operation.

## LC Tank Circuit Design

### Resonant Frequency
```
f0 = 1 / (2π × √(L × C))
```

### Quality Factor
```
Q = (1/R) × √(L/C)
```

Where R is the total resistance in the circuit.

### Bandwidth
```
BW = f0 / Q
```

### Impedance at Resonance
```
Z = √(L/C) / R  (for series resonance)
Z = R × √(L/C)  (for parallel resonance)
```

## RF Power and Range Calculations

### Power Density
```
P_density = P_transmit / (4π × r²)
```

Where:
- **P_transmit**: Transmitter power
- **r**: Distance from transmitter

### Effective Radiated Power (ERP)
```
ERP = P_transmit × G_antenna
```

Where G_antenna is the antenna gain.

### Friis Transmission Equation
```
P_received = P_transmit × G_tx × G_rx × (λ / 4πr)²
```

## Jamming Effectiveness

### Signal-to-Noise Ratio
```
SNR = P_signal / P_noise
```

### Jamming-to-Signal Ratio
```
J/S = P_jammer / P_signal
```

**Effective jamming occurs when:** J/S > 1 (0 dB)

## Frequency Response Limitations

### BJT Cutoff Frequency
```
fT = gm / (2π × (Cbe + Cbc))
```

Where:
- **gm**: Transconductance
- **Cbe, Cbc**: Junction capacitances

### Gain-Bandwidth Product
```
GBW = Gain × Bandwidth = constant
```

## Design Trade-offs

### Frequency vs Power
- Higher frequency → Lower transistor gain
- Lower frequency → Higher power capability

### Efficiency vs Linearity
- Class C: High efficiency, high distortion
- Class A: Lower efficiency, linear operation

### Range vs Frequency
- Higher frequency → Better antenna efficiency
- Lower frequency → Less path loss

## Practical Design Considerations

### Component Tolerances
```
f_actual = f_nominal ± (tolerance_L + tolerance_C)
```

### Temperature Effects
```
f(T) = f(T0) × [1 + α(T - T0)]
```

Where α is the temperature coefficient.
