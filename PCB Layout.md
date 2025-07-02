## Outline
- On Mech 2 Layer
- Move lines to desired shape
- Define board to given shape `D-S-D`
- Define Keep Out to given shape `D-S-P`
	- set size to 0.3mm
	- delete previous shape

## Layer Manager
- Get Layer Manager `D-K`
- Get template
	- File -> Load Stackup from Server
	- Fix the dielectrix thickness so overall PCB is 1.6mm. See standard FR4 thicknesses. Set PCB thickness depending on needs (0.8mm to 1.6mm for example). Can depend on High speed data lines (for example)

## Rules
- Get Design Rules `D-R`
- Electrical -> Clearance: Set min
- Routing -> Width: Set min
- Options
	- 5/5mils (0.15mm)
	- 4/4mils (0.127mm)
	- 3/3mils (0.1mm)

## Placement
- Design -> Import Changes from XXX
- Place components in a box 
	- PCB Panel
	- Make sure `Select` is enabled
	- Select all components
	- `T-O-L`
- Organize components in sections
	-  Select from schematic
	- `T-O-L`

## Routing
- After placing components, route tracks 
	- Vias
		- 0.5/0.3
		- 0.45/0.25
		- 0.4/0.2 (only if absolutely necessary)
- Make sure high power tracks are wide enough
- Make sure data tracks are impedances matched if necessary
- For power vias, no need to thermal relief, do direct connect
- For via under BGA/LGA, use plugged/capped via (plugged with epoxy or soldermask ink, allows for better surface and no risk of solder leakage)
- Place test pads on vias for added mechanical strength

### Vias
- Plated
	- Plated the copper via with HASL or ENIG
- Tenting
	- Soldermask is applied to via instead of plating with HASL or ENIG
- Plugged
	- Epoxy fills the holes after copper, prior to plating or soldermask application

## Planes and Polygons
- Once all the tracks are routed, route the power with power polygons
- Polygon Manager `T-G-M`
- Depending on the number of layers, here are the options
	- 4 Layers
		- L1: Signals (Power if convenient and on the outside)
		- L2: Power or GND (Signal if necessary)
		- L3: Power or GND (Signal if necessary)
		- L4: Signals (Power if necessary)
- Location of ground depends on the signals on L1 or L4. For example, if USB on L1, set L2 to GND
- Stich Plane Islands together
- Use Via Stitching to do this as well

## Finishing Design
- Via stitching (Shelve all the polygons that aren't connected to ground)
- Via tenting: puts solder mask over the via to prevent shorting. Make sure the Rule is enabled, and each via follows the Rule in the via properties
- Teardrop: track teardrop to help manufacturing
- Set pads to "Rouded Rectangle 10%". Use "Find Similar", set Parameters "Pads" and "Shape" to same, with Shape being "Rectangular"
- Complete silkscreen
	- Width min: 0.12mm
	- Height min: 0.6mm
	- Can set over via
- Make sure the correct variation is applied, and correct part are DNP
- Add dimensions to board
- Check 3D components

## DRC
- Complete DRC
- Waive Warning if necessary (Solder Bridge for example) and add reason


## Notes
- in cases with two caps, put smallest closer to component
- As much as possible, enter pad in-line with it's direction