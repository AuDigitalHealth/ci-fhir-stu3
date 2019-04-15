#### Normative changes in this profile
The following specific changes were made:
1. `Practitioner.identifier`
- identifier cardinality constrained to [1..\*]
- mandatory HPI-I [1..1]
1. `Practitioner.identifier`
- added a slice for *Employee Number*
1. `Practitioner.name`
- constrained to the [Agency HumanName Base profile](StructureDefinition-humanname-dh-base-1.html)
1. `Practitioner.photo`
- zero (explicitly prohibited)

#### Examples
The following examples have been added:
