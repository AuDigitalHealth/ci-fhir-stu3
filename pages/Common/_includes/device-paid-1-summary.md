#### Normative changes in this profile
The following specific changes were made:
1. `Device.identifier`
- identifier cardinality changed from [0..\*] to [1..\*]
- PAI-D identifier cardinality changed from [0..\1] to [1..\1]
1. `Device.type`
- changed the ValueSet binding strength to 'extensible'
1. `Device.patient`
- constrained to the [Agency Patient Base profile](StructureDefinition-patient-dh-base-1.html)
1. `Device.owner`
- constrained to the [Agency Organization Base profile](StructureDefinition-organization-dh-base-1.html)

#### Examples
1. [Maximal example for Device with PAI-D identifier slice](Device-devicePAID-max-example.html)