A specification document outlines the requirements for a given project.
It contains requirements, validation method, team allocation, naming scheme, etc.

See Evera (P145) Specification Document for a good example, or BeOneBreed

Should take 10hrs for a mostly complete preliminary doc. 

- Answers to the question "What"
- Does **not** answer the question "How", unless pre-specified point by client
- Can be low or high level depending on context
- Requirements consider:
	- project context
	- performance
	- cost
	- norms/standards
	- environment
- Must be:
	- clear
	- ***verifiable*** by
		- test
		- analysis (datasheet/theory)
		- inspection (usually visual)
	- measurable
	- cover function and non-functional needs
	- identifies validation method, not test specifications
- No technical solutions
- 1 requirements, 1 test
- Specify team allocation for each (mech, elec, software)
- Allows to set goals and end of project cycle
- details the deliverables for the client
- guides product development
- To verify a specifications document, read line-by-line and draw an architecture
- Add the verification method of the requirements when it's written (immediately)
- The section "system" is not purely requirements, mostly to explain the sections. The names given here must be found in each respective section.
- Each section must have the System requirement at the beginning to remind the section what it's about
- Most requirements use "The System" as the subject to keep it high level, unless the requirements specifically talks about a component
- Remember to add specific numbers to the requirements, even if they are TBC
- In a section, organise requirements by topics in a logical manner
- Maske sure functions are differentiated
- Each section found in the specification document must be a section in the Architecture
- Requirements need to talk about functionality, behavior, needs, applications, modes
- Start with a blank page and very high level behavior/function/modes sentences
	- Break down or separate each sentence into derived requirements
	- The sentences are the sections of the specifications document
	- the derived requirements must say who controls and is compatible with who
		- eg. " Sensor piloté par coeur principal et compatible avec le système d'exploitation"
- Length of a requirement doesn't matter it is clear
- Include a system overview and explanation of the system
	- Can be in a separate document like P270
	- Can be in the 1st page of the spec document like P269
	- 
