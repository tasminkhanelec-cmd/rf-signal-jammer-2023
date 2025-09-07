# Frequency Calculations

## Timer Circuit (NE555 IC)

### Design Formula
The NE555 configured as astable multivibrator generates the base frequency:

```
f = 1.44 / ((R1 + 2R2) × C1)
```

### Duty Cycle Calculation
```
Duty Cycle = (R1 + R2) / (R1 + 2R2) × 100%
```

### Target Specifications
- **Target frequency**: ~500 kHz
- **Purpose**: Generate pulse with high-frequency harmonics
- **IC limitations**: Compatible for 2-3 MHz range maximum

### Component Selection Impact
- **R1, R2**: Control frequency and duty cycle
- **C1**: Primary frequency determining capacitor
- **C2**: Decoupling capacitor (no effect on frequency)

## Tank Circuit (LC Resonance)

### Resonant Frequency Formula
```
f = 1 / (2π × √(L × C))
```

### Design Values
- **L1**: 6.287 nH (inductor)
- **C1**: 0.268 pF (capacitor) 
- **Calculated resonant frequency**: 3877.3 MHz

### Calculation Example
```
f = 1 / (2π × √(6.287 × 10⁻⁹ × 0.268 × 10⁻¹²))
f = 1 / (2π × √(1.685 × 10⁻²¹))
f = 1 / (2π × 1.298 × 10⁻¹¹)
f = 3877.3 MHz
```

## Frequency Limitations

### Hardware Constraints
1. **BF422 BJT**: Operating frequency range ~100 MHz
2. **Component tolerances**: Affect precise frequency tuning

### Achieved vs Theoretical
- **Theoretical (Tank Circuit)**: 3877.3 MHz
- **Practical Achievement**: ~100 MHz
- **Limiting Factor**: BJT frequency response bandwidth

## High-Frequency Harmonics

The timer output contains multiple frequency components:
- **Fundamental**: ~500 kHz
- **Harmonics**: Multiple frequencies up to BJT limit
- **Useful Range**: Up to 100 MHz with BF422 transistor
