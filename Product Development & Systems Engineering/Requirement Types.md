#### Operational Requirement
- Very abstract/high level
- Written in system-as-a-whole terms, internal workings are not revealed
- What does the whole system need to accomplish, and how well?
- Who and what will the system be interacting with externally?
- What are the most likely environments the system will be operating within?
- Documented in Stakeholder Requirements Specification (StRS)
- Requirements describes the effectiveness measures that assure success of the system (Measure of Effectiveness - MOE)
#### Performance Requirement
- A quantitative measure characterizing a physical or functional attribute relating to the execution of an operation or function
- Performance attributes include: 
	- quantity (how many or how much)
	- quality
	- coverage (how much area, how far)
	- timeliness (how responsive, how frequent)
	- readiness (availability, mission/operational readiness)
- Can be high, mid or lower level
- Describes system-as-a-whole or lower level characteristics
- Minimal acceptable value that is necessary to satisfy the mission. What is the minimum value system effectiveness can be achieved? (Threshold)
- Value desired by the user/stakeholder. Maximum feasible value necessary to satisfy the mission. What is the maximum value system effectiveness can be achieved) (Objective)
- How well must it interact with other elements - external or internal?
- Documented in [[System Requirements Specification]] (SyRS)
#### Functional Requirement
- Can be high, mid or lower level
- Describes behaviors of the system-as-a-whole, or behaviors of the lower level elements
- What must the entity do? (Activities)
- Always expressed in verb/noun context
- What other elements must it interact with and how?
- What are the expected inputs and outputs? (FEDS-M -> Forces, Energy, Data, Signals, Materials)
#### Constraint Requirement
- Can be high, mid or lower level
- Restricts the range of possible outcomes
- What must the entity contain?
- What must the entity interact with? Eg. :
	- Standards and outside specs
	- Size, weight, shape, color, material, etc.
	- Interface standards
- Documented in any specification in the spec tree, most common at the lowest design specification level
#### Interface Requirement
- Can be high, mid or lower level
- Describe the relationships to/from elements inside or outside of the system of interest
- Describes specific format content, order of operations for functional intersections (eg. Bluetooth, USB, MIL-STD-1553B)
- What range of inputs is the system expecting?
- What range of outputs will the system provide?
- With user-in-the-loop, use cases are conducted and result in the development of a User Interface Specification
- Documented in the Interface Control Documents (ICD) and Interface Requirements Specification
#### Verification Requirement
- Can be high, mid or lower level
- Describe compliance with another type of requirements (capability, performance, functional, etc.)
- How will compliance be verified?
- Always link to another requirement
- Describes verification method
	- Inspection
	- Analysis
	- Demonstration
	- Test
	- Similarity
- Documented in the same spec as the original requirements
- Verification results are reported in verification test results document
#### Validation Requirement
- High level, mission oriented
- Expressed in use case driven scenarios or mission scenarios
- How effective is the system at performing the mission(s)?
- How suitable is the system for use/sustainment in the operational environments(s)?
- Has the right system been built for the job?
- Initial requirements are documented in Stakeholder Requirements Specification (StRS)
- Validation results are documented in a Validation Report