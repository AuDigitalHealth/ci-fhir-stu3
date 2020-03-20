#### Provenance for the Generation of a List *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
* A clinical information system (CIS) sends or receives a list with provenance with the My Health Record system
* A contracted service provider (CSP) sends or receives a list with provenance with the My Health Record system
* A CIS sends or receives a list with provenance with another CIS or CSP
* A CSP sends or receives a list with provenance a CIS or another CSP
* A registered portal or registered repository receives a list with provenance

An expected usage scenario, further scoping the above overarching scenarios is:

* Prescription and dispense view (PDV) exchanged with the My Health Record as a list with provenance

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* When creating a list as a filtered view of an existing list (e.g. filtering to only current medicines), the source list can be identified using the entity element with an entity.role of 'source' and entity.whatReference pointing to that source list resource
* If a list has been generated from a time-based query or time-based filter it is expected that filtering dates are captured in the provenance period with the earliest filtering date provided in the period start and the latest filtering date provided in the period end
* When creating the list  the list is created with a set of existing resources, e.g. AllergyIntolerance, the resources that initially populated the list may be referenced as entities with the role of 'source' and what pointing to that resource

When the list is a prescription and dispense view it is expected that:
* only one instance of agent (the assembling device e.g. My Health Record system) is provided
* only one instance of target (the Prescription and dispense view list resource) is provided
