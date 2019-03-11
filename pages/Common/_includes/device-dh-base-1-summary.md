#### Normative changes in this profile
The following specific changes were made:
1. `Device` root element
- added invariant: *The Device shall have either `identifier` or `type` or `udi.name`*
1. `Device.type`
- changed the ValueSet binding strength to 'extensible'
1. `Device.patient`
- constrained to the [Agency Patient Base profile](StructureDefinition-patient-dh-base-1.html)
1. `Device.owner`
- constrained to the [Agency Organization Base profile](StructureDefinition-organization-dh-base-1.html)

#### Examples
1. [Minimal example for Device](Device-device-min-example.html)
1. [Maximal example for Device with all identifier slices](Device-device-max-example.html)