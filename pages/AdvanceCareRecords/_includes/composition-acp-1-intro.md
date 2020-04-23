#### Advance Care Planning *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage Scenarios

The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) sends or receives an advance care planning document with the My Health Record system
* A contracted service provider (CSP) sends or receives an advance care planning document with the My Health Record system
* A CIS sends or receives an advance care planning document with another CIS or CSP
* A CSP sends or receives an advance care planning document with a CIS or another CSP
* A registered portal or registered repository receives an advance care planning document

An expected usage scenario, further scoping the above overarching scenarios is:

* A Goals of Care (GoC) advance care planning document

A system may be a producer by attaching the Advance Care Plan document to the Document Reference, constructing a Composition resource and sending that set of resources.

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that:

* TBD

When sending to the My Health Record system it is expected that:

* all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).

Additionally, when the document that is referenced is a goals of care document it is expected that:

* title will contain 'Goals of Care'
* section title will contain 'Goals of Care'