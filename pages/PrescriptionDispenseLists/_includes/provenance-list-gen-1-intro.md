### Provenance for the Generation of a List *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios
* A clinical information system (CIS) sends or receives a list with provenance with the My Health Record system
* A contracted service provider (CSP) sends or receives a list with provenance with the My Health Record system
* A CIS sends or receives a list with provenance with another CIS or CSP
* A CSP sends or receives a list with provenance a CIS or another CSP
* A registered portal or registered repository receives a list with provenance

An expected usage scenario, further scoping the above overarching scenarios is:

* Prescription and dispense view (PDV) exchanged with the My Health Record as a list with provenance
Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.


##### Implementation guidance

For the supported scenarios in this implementation guide:

* Where the list is a filtered view of an existing list, the source list may be referenced as an entity with the role of 'source' and what pointing to that list resource
* Where the list is created with a set of existing resources, e.g. AllergyIntolerance, the resources that initially populated the list may be referenced as entities with the role of 'source' and what pointing to that resource
* Where the generated list is a filtered view of an existing list, or a source system, or generated from a time-based search query it is expected that filtering dates are captured in the provenance period with the earliest filtering date provided in the period start and the latest filtering date provided in the period end

#### When the list is a PDV
* It is expected that the only agent provided is the assembling device
* It is expected that there is only one instance of target, which is the Prescription and dispense view list resource