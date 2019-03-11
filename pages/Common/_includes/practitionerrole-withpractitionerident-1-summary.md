#### Normative changes in this profile
The following specific changes were made:

<!--
1. `PractitionerRole`
- added an invariant such that a practitioner or an organisation must be present
-->
1. `PractitionerRole.practitioner`
- exactly one and constrained to the [Agency Practitioner with mandatory identifier profile](StructureDefinition-practitioner-ident-1.html)
1. `PractitionerRole.organization`
- constrained to the [Agency Organization Base profile](StructureDefinition-organization-dh-base-1.html)
1. `PractitionerRole.code.coding`
- optional slice for coding with required terminology binding to reference [National Clinical Terminology Service ValueSet for Australian and New Zealand Standard Classification of Occupations](https://healthterminologies.gov.au/fhir/ValueSet/anzsco-1)
- optional slice for coding with required terminology binding to reference [National Clinical Terminology Service ValueSet for SNOMED CT](https://healthterminologies.gov.au/fhir/ValueSet/practitioner-role-1)

<!--
#### Examples
The following examples have been added:
1. [Minimal example Practitioner Role](PractitionerRole-practitionerrole-min-example.html)
1. [Maximal example for Practitioner Role with all identifier slices](PractitionerRole-practitionerrole-max-example.html)
-->
