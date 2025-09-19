## Companies to get batteries from:
- Grepow
- EEMB
- PK cell
- EVE

## General Notes
- Remember that batteries have internal leak current that varies on temperature, voltage, age of batteries, chemistry

## Battery Types
- Primary: Non-rechargeable
- Secondary: Rechargeable

## Battery Protection
- Voltage Protection
	- Overcharge Protection: Voltage threshold when the charging will stop. To test, when a battery is almost full, increase the charging voltage until the circuit opens. For Li-ion/LiPo, fully charged is 4.2V, so set power supply to 4.3V or 4.4V, limit the current, and check when it opens.
	- Overdischarge Protection: Voltage threshold when the discharging will stop. To test, discharge the battery at a constant current. When almost discharged, set small current to find the threshold with most accuracy. Check when the circuit opens. Measure the cells after the protection circuit if possible to see the voltage threshold.
- Current Protection
	- Overcharge Protection: Limits the charging current in a battery. To test, charge the battery, and increase the current until it opens the circuit. Can test slow and fast increase to find both thresholds. This is especially used for Li-ion who have a 10C-20C charging capacity, so must limit the input current.
	- Overdischarge protection: Limits the discharge current in a battery. To test, set the current close to the value, and increase incrementally until the circuit opens. Equivalent to partial short circuit protection, which means only a few amps can pass, but it can still be too much for the board
	- Short Protection: Limits the discharging current in a battery. To test, use the short function on an E-load.  This protection should open the circuit quickly when a full short circuit is encountered.
- 
- Capacity: To test, use the battery function on the E-load with the proper parameters
- Temperature Monitoring: Include an NTC on the board for temperature monitoring and management
- Cell Balancing: Protection circuit should keep the different cell voltage relatively close to not create odd conditions where cells charge and discharge into themselves.
## Li-ion

Type: Secondary battery

Nominal Voltage: 3.7V
Charging Voltage: 4.2V
Discharge Voltage: 3.0V

Protection PCB Specs:
- Charging Max Voltage: ~4.3V
- Discharged Min Voltage: ~2.8V

Temperatures from -20C to 80C in certain cases. Can achieve high discharge rates, small sizes, etc.

They generally come in cylindrical formats: 18650/21700
They can be customized with protection PCBs, NTC Thermistors and connectors
## LiPO

Type: Secondary battery

Similar to Li-ion, but in pouches.

## LiFePO4

Type: Secondary battery

Nominal Voltage: 3.2V
Charging Voltage: 3.6V
Discharge Voltage 2.6V (around)

Similar temperature ratings

Advantages over the other chemistries is related to lower cost, high safety (chemical stability), long life  cycles
Used in EV applications and battery backups

## LiSOCl2

Type: Primary battery

Nominal Voltage: 3.6V
Charging Voltage: 3.6V
Discharge Voltage 3.45V (around)