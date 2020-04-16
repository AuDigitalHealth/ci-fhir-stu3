#### RelatedPerson with Mandatory Identifier  *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is recommended that:
* an Australian address conforms to [AU Base Address](http://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-address.html)

When sending an advance care record to the My Health Record system it is expected that:
* an IHI-I will be sent
* family name will be sent

This profile is referenced by [Advance Care Directive Custodian Record](StructureDefinition-composition-acdcr-1.html), [Advance Care Planning](StructureDefinition-composition-acp-1.html) and [Advance Care Planning Document Reference](StructureDefinition-documentreference-acp-1.html).