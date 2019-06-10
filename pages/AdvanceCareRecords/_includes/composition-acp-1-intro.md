### Advance Care Planning *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### **Usage Scenarios**
The following are the usage scenarios expected:

* A clinical information system (CIS) sends or receives an Advance Care Plan with the My Health Record system
* A contracted service provider (CSP) sends or receives an Advance Care Plan with the My Health Record system
* A CIS sends or receives an Advance Care Plan with another CIS or CSP
* A CSP sends or receives an Advance Care Plan with a CIS or another CSP
* A registered portal sends or receives an Advance Care Plan
* A registered repository receives an Advance Care Plan

A system may be a producer by attaching the Advance Care Plan document to the Document Reference, constructing a Composition resource and sending that set of resources.
##### **Implementation guidance**
For the expected usage scenarios in this implementation guide:

* It is required that the composition include only the specified top-level section; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.