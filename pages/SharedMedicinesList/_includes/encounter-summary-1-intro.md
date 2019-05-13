### Encounter for a Shared Medicine List *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios
* A summary of an encounter between a patient and a healthcare provider exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.


##### Implementation guidance

For the expected usage scenarios in this implementation guide:

* It is expected that the status will be 'finished'. 

 
Known issue: 
* BR 028349 Attribute for Healthcare Setting describes these: “Hospital Pharmacy”, “Home Medicines Review”, “Dose Administration Aids”, “Community Pharmacy” or “Residential Care”.
Dose Administration Aid is a device or a system for organising doses of medicines according to the time of administration. Value 'Dose Administration Aids' does not fit into the healthcare setting. Check if this requirement is aiming at showing that the PSML is created by DAA packing pharmacy and as such may not include all other medicines a patient is taking. A DAA packing pharmacist should take all necessary steps to assure that the PSML includes a list of all medicines a patient is taking and not only those packed in a DAA before creating a document; work-flow issue. May be related to HL7 AU discussion about representing packed medicines in a medicine list.

