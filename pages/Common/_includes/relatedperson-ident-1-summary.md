#### Normative changes in this profile
The following specific changes were made:
1. `RelatedPerson.identifier`
- constrained cardinality of RelatedPerson.identifier to [1..\*]
1. `RelatedPerson.name`
- constrained to the [Agency HumanName Base profile](StructureDefinition-humanname-dh-base-1.html)
1. `RelatedPerson.patient`
- constrained to the [Agency Patient Base profile](StructureDefinition-patient-dh-base-1.html)
1. `RelatedPerson.photo`
- zero (explicitly prohibited)
