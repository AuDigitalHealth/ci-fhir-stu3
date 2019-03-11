This structure is derived from the [HL7 AU Base Composition](https://build.fhir.org/ig/hl7au/au-fhir-base//StructureDefinition-au-composition.html)

This profile introduces the following variations from the above profile:
1. Exactly one `language` as 'en-AU'
1. `subject` as Patient with mandatory IHI
1. Exactly one `author` as Patient with mandatory IHI or RelatedPerson with mandatory IHI
1. zero `confidentiality` (explicitly prohibited)
1. Exactly one `custodian` as Organization with mandatory identifier