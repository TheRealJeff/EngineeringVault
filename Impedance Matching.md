Impedance matching is the practice of designing and/or adjusting the input or output impedance of a system to match a desired value on transmission lines.

[Wiki](https://en.wikipedia.org/wiki/Impedance_matching)

## Maximum Power Transfer
The impedance can be matched to ensure maximum power transfer between an input and an output. To accomplish this, complex conjugate matching is used.

$Z_{load} = Z^*_{source}$

## High Speed Signal Reflection
In general, the methods described here are needed when the transmission line is longer than the critical length, which can be considered as 1/10 of the wavelengths as a rule of thumb.

Otherwise, a more in depth view is [here](https://resources.altium.com/p/why-there-transmission-line-critical-length)

These techniques revolve around reducing the amount of reflections in the transmission line, see examples [here](https://resources.altium.com/p/why-impedance-matching-important-transmission-line). This is important for high speed signals, such as USB, HDMI, RF, etc.

The main methods to complete impedance matching are to add simple elements (resistors, capacitors, inductors) and bring the impedance to the desired value. This technique is illustrated in these documents:
- [General Matching](https://abracon.com/uploads/resources/Abracon-White-Paper-Antenna-Impedance-Matching.pdf)
- [NFC Reader Matching](https://www.ti.com/lit/an/sloa135a/sloa135a.pdf?ts=1692189116126)
- 