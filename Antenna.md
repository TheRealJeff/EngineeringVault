# Testing

## 1. Signal Strength Testing
When evaluating what antenna to use for a product, meaning comparing only the antennas, apples to apples, use the following format:

1. Space the TX antenna and RX antenna at ~1m distance
2. Place the antennas in a RF quiet area (avoid routers, noise, other RF devices)
3. Select a single power level to do the test. Choose it based on receiving a ''clean'' signal, one that its high enough above the noise floor (has good SNR)
4. Observe the RX signal strength

This test is similar to doing RSSI testing with a product.
## 2. Radiation Pattern Testing
1. Install the antenna in the same environment as the previous test
2. Turn the product on itself at specific angles (add 15° for every step)
3. Create a 2D map of the radiation pattern

## 3. Environmental Testing
1. Install the antenna in the same environment as the first tests
2. Add a different material backing
	1. Metal
	2. Plaster (gyprock)
	3. Concrete
3. Observe the difference the in signal strength


# Interpreting Results from Past Tests

In this test, the "Reference" antenna is from the nRF52840-DK. It is a built-in trace antenna used as a reference.

The external antennas were tested using a SWF-to-SMA cable on the provided connector located on the DK. The nRF Connect for Desktop mode "Direct Test Mode" was used to send a tone, and a spectrum analyzer with a directional antenna was the RX antenna.

Here, there seems to be a large discrepancy between the performance of the external antennas and the built-in one. In this test, a large aluminum metal backing (stencil sheet for PCBs) was added to create a simulation of a product installation. A reason to explain this is that the built-in antenna is designed to utilize the strong electro-magnetic interactions between the metal sheet that is acting as a virtual ground. The external antennas are not made to accomplish the same thing, and instead have their performance negatively affected by the sheet.
![[Pasted image 20250212110323.png]]
![[Pasted image 20250212113246.png]]

# Constructive Reflections for Antenna Placement Near Metal Plate

To achieve constructive reflections from a metal plate, the antenna should be positioned at a distance that corresponds to an odd multiple of a quarter-wavelength ($\lambda/4$) of the operating frequency. This ensures that the reflected wave is in phase with the direct wave, reinforcing the signal.

## Distance Formula
The distance \( $d$ \) from the metal plate to the antenna can be calculated as:

$$
d = \left( n + \frac{1}{4} \right) \lambda
$$

Where:
- \( $d$ \) = Distance from the metal plate to the antenna  
- \( $n$ \) = 0, 1, 2, 3, ... (any non-negative integer)  
- \( $\lambda$ \) = Wavelength of the signal, calculated as:

$$
\lambda = \frac{c}{f}
$$

- \( $c$ \) = Speed of light ( $3 \times 10^8 \, \text{m/s}$ \)  
- \( $f$ \) = Frequency of the signal in Hz  

## Practical Example
For a signal at 2.4 GHz (e.g., Wi-Fi frequency):

- \( $\lambda = \frac{3 \times 10^8}{2.4 \times 10^9} = 0.125 \, \text{m}$ \)  
- The first constructive distance would be:

$$
d = \left( 0 + \frac{1}{4} \right) \times 0.125 = 0.03125 \, \text{m} = 3.125 \, \text{cm}
$$

Subsequent distances would be at odd multiples:
- \( $3\lambda/4 = 9.375 \, \text{cm}$ \)  
- \( $5\lambda/4 = 15.625 \, \text{cm}$ \)  
- and so on...

## Considerations
Choose the distance based on practical constraints and the desired gain or beam pattern.

