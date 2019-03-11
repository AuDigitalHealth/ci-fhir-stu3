#### Normative changes in this profile
The following specific changes were made:
1. `Patient.identifier`
- constrained cardinality of Patient.identifier to 1..*
1. `Patient.name`
- constrained to the [Agency HumanName Base profile](StructureDefinition-humanname-dh-base-1.html)
1. `Patient.contact.relationship`
- changed terminology binding to better categorise the relationship that the contract person has with the patient
1. `Patient.contact.name`
- constrained to the [Agency HumanName Base profile](StructureDefinition-humanname-dh-base-1.html)
1. `Patient.contact.organization`
- constrained to the [Agency Organization Base profile](StructureDefinition-organization-dh-base-1.html)
1. `Patient.photo`
- zero (explicitly prohibited)
1. `Patient.animal`
- zero (explicitly prohibited)
1. `Patient.generalPractitioner`
- constrained to use either the [Agency Organization Base profile](StructureDefinition-organization-dh-base-1.html) or the [Agency Practitioner Base profile](StructureDefinition-practitioner-dh-base-1.html)
1. `Patient.managingOrganization`
- constrained to the [Agency Organization Base profile](StructureDefinition-organization-dh-base-1.html)

#### Examples
The following examples have been added:
1. [Minimal example Patient](Patient-patient-min-example.html)
1. [Maximal example Patient](Patient-patient-max-example.html)
1. [Patient example with identifier slices](Patient-patient-with-identifier-slices-example.html)