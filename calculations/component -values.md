# Component Values and Selection

## Timer Section (NE555)

### Resistors
- **R1, R2**: Timing resistors for frequency control
- **Selection criteria**: 
  - Target frequency ~500 kHz
  - Reasonable duty cycle (40-60%)
  - Standard resistor values available

### Capacitors
- **C1**: Main timing capacitor (varies with design)
- **C2**: Decoupling capacitor for control pin
- **DC blocking capacitor**: 4.7 μF (couples timer to amplifier)

## Power Amplifier Section (BF422 BJT)

### Transistor Selection
- **Model**: BF422 NPN BJT
- **Type**: RF transistor for high-frequency applications
- **Operating range**: Up to ~100 MHz
- **Configuration**: Class C amplifier

### Biasing Components
- **Rb (Base resistor)**: 5.6 kΩ
- **Purpose**: Pull base below cutoff point
- **Effect**: Ensures Class C operation (conduction angle < 180°)

## Tank Circuit Components

### Inductor
- **L1**: 6.287 nH 
- **Type**: Air core 
- **Function**: Energy storage and frequency tuning
- **Selection**: Based on target resonant frequency

### Capacitors
- **C1**: 0.268 pF (tuning capacitor)
- **Additional capacitors**: 3.3pF, 47μF, 0.268pF, 0.7878pF, 47pF
- **Purpose**: Fine-tuning and coupling between stages

## Additional Components

### Power Supply
- **Voltage**: 9V DC battery
- **Current**: Sufficient for Class C amplifier operation
- **Regulation**: Battery provides stable DC source

### Antenna
- **Type**: 24 AWG wire coil
- **Length**: Optimized for ~100 MHz
- **Range**: Approximately 1 meter effective jamming distance

### Miscellaneous
- **LED**: Power indicator
- **Switch**: Circuit on/off control
- **Various resistors**: 25Ω, 5.6kΩ, 0.1kΩ, 10kΩ for different functions

## Component Selection Rationale

### Frequency-Related Choices
1. **Timer components**: Selected for ~500 kHz base frequency
2. **Tank circuit**: Calculated for theoretical 3877 MHz resonance
3. **BJT selection**: Limited practical frequency to 100 MHz range

### Power and Efficiency
1. **Class C configuration**: Maximum efficiency (~90% theoretical)
2. **Component ratings**: Adequate for expected power levels
3. **Coupling methods**: AC coupling between stages

### Practical Constraints
1. **Available components**: Standard electronic component values
2. **Cost considerations**: Educational project budget
3. **Measurement capability**: Compatible with available test equipment
