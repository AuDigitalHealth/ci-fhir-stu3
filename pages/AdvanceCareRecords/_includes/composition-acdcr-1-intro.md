#### Advance Care Directive Custodian Record *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage Scenarios
The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) receives an Advance Care Directive Custodian Record
* A contracted service provider (CSP) receives an Advance Care Directive Custodian Record
* A registered portal sends or receives an Advance Care Directive Custodian Record
* A registered repository receives an Advance Care Directive Custodian Record

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that:

* It is required that the composition include only the specified top-level section; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.

When sending an Advance Care Plan to the My Health Record system it is expected that all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).  