## Applications
### Voltage Dividers

Things to check:
- Leak current
- That the resistance isn't so high that it can't drive the ADC pin

#### Calculations
### Current Sense Resistors

- Choose a resistor that can dissipate the power that flows through, without being too low that it can't read the voltage drop accurately

### Pull-Up/Pull-Down Resistors
- Given that most applications have batteries, find the value that gives a proper MCU voltage high or low without leaking too much
- Should be based on the type of GPIO (types changed from MCU to MCU)
	- Internal pull-up or pull-down
	- High impedance


## How to Choose
- Dissipation power
- Tolerance (1% is standard, anything lower is pricier)
- Package
- 

## Types

[Thin vs. Thick-Film](https://eepower.com/resistor-guide/resistor-materials/thin-and-thick-film/#)
### Thin-film

### Thick-film
More temperature resistant

### Ceramic