#### Advance Care Directive Custodian Record *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage Scenarios
The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) sends or receives an Advance Care Directive Custodian Record with the My Health Record system
* A contracted service provider (CSP) sends or receives an Advance Care Directive Custodian Record with the My Health Record system
* A CIS sends or receives an Advance Care Directive Custodian Record with another CIS or CSP
* A CSP sends or receives an Advance Care Directive Custodian Record with a CIS or another CSP
* A registered portal sends or receives an Advance Care Directive Custodian Record
* A registered repository receives an Advance Care Directive Custodian Record

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that:

* It is required that the composition include only the specified top-level section; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.

When sending an Advance Care Directive Custodian Record to the My Health Record system it is expected that all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).  