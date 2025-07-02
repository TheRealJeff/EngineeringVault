# Connectors
- Connectors with a through-hole mounting are the best
- Avoid using identical connectors with different functions on a product
- Choose a connector with good polarization (can only be plugged one way)
- Connectors with supply voltage should have sockets and not pins
- Connectors with metal frames require less ESD protection
- Use connectors that have 10% more pins for future proofing
- Connector pins should not carry more than 50% of the rated current
- Connectors should operate in an environment no more than 25°C below the maximum rated temperature

# Resistors
- Resistors with a resistance below 1MΩ are considered ideal below 10MHz
- 0Ω resistors have a maximum current capability of 1-2A
# Capacitors
- At low frequency, capacitors behave regularly. At the resonant frequency, the impedance is reduce to close to 0. Above the resonant frequency, capacitors behave as inductors, and the phase is inverted 180°
- Liquid electrolytics capacitors:
	- Good capacitance to cost ratio
	- Low lifetimes
	- Low resonant frequency
	- High ESR
	- Polarized
	- Large footprint
	- High leakage current
	- Limited shelf life
- Ceramic capacitors:
	- 3 Character code: minimum temperature, maximum temperature, capacitance variance over temperature range
	- Class 1 (C0G, NP0): Capacitance values stable against voltage, frequency and temperature. Low losses, used for filters, timers and high frequency circuits
	- Class 2 (X7R, Y5V): Higher capacitance at the expense of variability with voltage, frequency, temperature and age. Piezoelectric vibration and shock can induce voltages. Used as decoupling capacitors, coarse filters, coupling capacitors for relatively high-level signals
	- Failure more: from mechanical stress, ceramic capacitors break and cause shorts. Solution is to place 2 capacitors in series at 90° from each other
# Inductors
- Power inductors: 
	- Optimized for high currents, but large SMD footprint
	- DC/DC converters
- RF Coils: 
	- Optimized high bandwidth and small size, but large DC resistance
	- High frequency filters
- Chokes: 
	- Optimized low-loss at DC, but high-loss at RF frequencies
	- Harmonic suppression
- Reasons for avoiding inductors
	- Less standardized footprints
	- More expensive due to complex 3D structure
	- High DC resistance (up to 1Ω)
	- Brittle ferrite core
	- Can saturate under high current application
- Methods to avoid
	- Use LDO instead of switching regulator
	- use active filter instead of passive 2nd order