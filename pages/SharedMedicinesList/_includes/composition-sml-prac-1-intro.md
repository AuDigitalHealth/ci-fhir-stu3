#### Shared Medicines List Authored by Practitioner *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios 

The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) sends or receives a practitioner authored shared medicines list document with the My Health Record system
* A contracted service provider (CSP) sends or receives a practitioner authored shared medicines list document with the My Health Record system
* A CIS sends or receives a practitioner authored shared medicines list document with another CIS or CSP
* A CSP sends or receives a practitioner authored shared medicines list document with a CIS or another CSP
* A registered portal or registered repository receives a practitioner authored shared medicines list document

An expected usage scenario, further scoping the above overarching scenarios is:
* A practitioner authored shared medicines list document exchanged as a pharmacist shared medicines list (PSML)

#### Implementation guidance 

For the overarching usage scenarios in this implementation guide it is expected that:

* where a sending system can state that a patient does not have an allergy or category of allergies an AllergyIntolerance will be sent
* where a sending system can state that a patient is not currently taking medication an Observation will be sent
* an empty section will be sent with an empty reason

When the shared medicines list is a PSML document it is expected that:

* status will be ‘final’
* composition author role will be a reference to a PractitionerRole resource that describes the author’s professional role, e.g. 159011008 \|Community pharmacist\|
* author will be a reference to a Practitioner resource that describes the author, e.g. the pharmacist
* encounter will be sent
* an allergies section will only be sent if at least one AllergyIntolerance can be sent
* a non-empty medications section will be sent and it will contain a List
* medications section content will be sent as either:
  * one section with the section.code '10160-0' History of Medication use Narrative, or
  * two sections, one with the section.code '101.32009' Current Medicines and one with the section.code '101.32027' Ceased Medicines