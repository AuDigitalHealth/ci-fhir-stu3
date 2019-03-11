#### Normative changes in this profile
The following specific changes were made:
1. `RelatedPerson`
- added an invariant such that the related person must have an identifier, a name or a relationship to the patient
1. `RelatedPerson.name`
- constrained to the [Agency HumanName Base profile](StructureDefinition-humanname-dh-base-1.html)
1. `RelatedPerson.patient`
- constrained to the [Agency Patient Base profile](StructureDefinition-patient-dh-base-1.html)
1. `RelatedPerson.photo`
- zero (explicitly prohibited)
