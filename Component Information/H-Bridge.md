H-Bridge design is relatively complex.

There are a few levels of complexity on the integrated to discrete component selection spectrum:

1. Fully integrated
Here, the IC will integrate the FETs and any control scheme required and feedback. Usually MCU pins will be needed to complete the controls
	1. Motor driver
	2. Full H-Bridge
	3. Half bridge (2, 3, 4, etc.)

2. Semi-integrated
Here, the IC will have some amount of control schemes inside the IC to drive the FETs
	1. Gate driver
	2. Motor driver
	3. Half-Bridge

3. Not integrated
Here, the IC will have very basic functionality
	1. Gate driver

## Key Differences: Half-Bridge vs Full-Bridge Gate Driver

| Feature                     | Half-Bridge Gate Driver        | Full-Bridge Gate Driver      |
|-----------------------------|--------------------------------|------------------------------|
| **Number of MOSFETs Controlled** | 2 (one high-side, one low-side) | 4 (two high-side, two low-side) |
| **Bootstrap Circuit Needed?**  | Yes (for high-side)         | Yes (for both high-sides)    |
| **Dead Time Control**        | Required                     | Required, often built-in     |
| **Protection Features**      | Limited, depends on IC       | Often has shoot-through prevention |
| **H-Bridge Control?**        | Requires 2 half-bridge drivers for full H-bridge | Single IC controls entire H-bridge |
| **Common Applications**      | DC-DC converters, half-bridge motor drivers | Full H-bridge motor drivers, Class-D amplifiers |

