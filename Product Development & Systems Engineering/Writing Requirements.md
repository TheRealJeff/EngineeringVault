Derivation: The creation of requirements based on an analysis of higher-order requirements

Allocation: The assignment of a requirement to one or more system elements within the architecture

Flow Down: Assignment a requirement to one of more lower level elements

Traceability: The creation of linkages from one system element to another

![[Pasted image 20231205144535.png]]
## Structure
- Western English sentence:
	- Subject, priority, verb, object
		- "The ATM_System shall provide Cash to the User"
	- Condition, Subject, Priority, Verb, Object
		- "Upon verifying Account_Balance available for Withdraw, the ATM_System shall provide Cash to the Customer"
	- Condition, subject, Verb, Object, Qualification
		- "After entering the Requested_Cash for Withdraw, the ATM_System shall provide the Requested_Cash, up to a maximum of $500"
- Subject: System itself (or some element of it)
- Priority: "Shall"
	- Based on Western legal system
	- "Will, may, should", etc. are not legally binding
	- Avoid "shall not", difficult to test (prove a negative)
## Guidelines
- Use [[Requirements Dictionary]]
- Single sentences
- Avoid conjunctions: and, or, then, as well as, but also, however, meanwhile, but, unless, otherwise, on the other hand, whereas, and/or
- If conjunctions are used, set in ALL CAPS: AND, OR, etc.
- Short statements
- Appropriate to the Level in the Hierarchy
	- Stakeholder level: "The SYSTEM shall..."
	- System requirements: "The \_\_\_ (system) shall..." or "The \_(subsystem) shall..."
	- Segment specifications: "The \_\_\_ (component) shall..."
- Active tense: "The User_Balance shall be displayed by the ATM_System" (*Passive*) vs. "The ATM_System shall display the User_Balance" (*Active*)
- Use Definite Article: "The ATM_System shall conduct Transactions for any person" (*Indefinite*) vs. "The ATM_System shall conduct Transactions for the User in the Operational_Environment" (*Definite*)
- Avoid ambiguity: all, many, some, several, minimal, best practices, user-friendly, generic, large, high-speed, small
- Must be quantifiable and measurable: Measures of Performance (MOPs), thresholds and objectives
- Quantify: be careful with <, > , =<, =>. Play devils advocate
- Necessary: system should be impossible to make without the requirement
- Appropriate: specific intent, desired capability, desired level of performance, functions or behavioral characteristics
- Unambiguous: all stakeholders in the requirement should understand the requirement the same way
- Complete: stand-alone, independent of other requirements, avoid cross-referencing, avoid pronouns
- Feasible: should not request impossible or unrealistic behaviors or features
- Verifiable: can the requirement be tested using one of the following methods:
	- Analysis
	- Demonstration
	- Test
	- Inspection

## Specification Practices
Specification...:
- Should be complete. No TBDs, blank placeholders, etc.
- Should contain all elements necessary to deliver intended end-item
- Should be consistent internally and externally with other specifications from earlier SDLC phases [[Product Life Cycle]]
- Should be feasible. Even if each requirement is feasible, it is possible the amalgam of requirements (the spec) is NOT feasible
- Must be validated. The spec should be able to prove that the delivered end item is valuable, useful, effective, suitable for use in the field