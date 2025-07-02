ESR: Equivalent Series Resistor rating: This is the equivalent resistance that one could add in a circuit to simulate a supercap

## Supercaps

High capacity capacitors that can have similar roles to batteries
Check:
- Leak current when charged
- Time to reach 100% charge
- ESR ratings (sometimes low)

## Tantalum Caps

High capacity density for the size

Check:
- Leak current (can be in the mA)

## Ceramic Caps

Capacitance can be lower when the applied voltage reaches the breakdown voltage rating (check datasheet)

## Aluminium Caps

They have trash ESR and low working hours
# Capacitor Bank
To calculate the capacitance required for a capacitor bank, use the following info and formulas:

$E=P \cdot t$

$E = \frac{1}{2} C V^2 \Longleftrightarrow C = \frac{2E}{V^2}$

$P\cdot t = \frac{1}{2} CV^2 \Longleftrightarrow C = \frac{2P \cdot t}{V^2}$

Solving for $C$ provides the capacitance. The above formulas assumes the voltage goes from $V$ to $0$. Instead, for a capacitor bank that will discharge from 24V to 12V while providing an amount of energy, use the following method

$\Delta E = E_i - E_f = \frac{1}{2}CV_i^2 - \frac{1}{2}CV_f^2 = \frac{1}{2}C(V_i^2-V_f^2)$

$\Delta E = \frac{1}{2}C(V_i^2-V_f^2)$


