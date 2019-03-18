This profile contains the following variations from [AU Base Medication Statement](http://hl7.org.au/fhir/StructureDefinition/au-medicationstatement):

* `medication[x]` as `medicationCodeableConcept`
* `informationSource` as [Base Patient](StructureDefinition-patient-dh-base-1.html), [Base Practitioner](StructureDefinition-practitioner-dh-base-1.html), [Base RelatedPerson](StructureDefinition-relatedperson-dh-base-1.html)
* `subject` as [Patient with mandatory Identifier  profile](StructureDefinition-patient-ident-1.html).
* Zero or one `reasonCode`
* Exactly one `dosage`
* `dosage` invariant: inv-dh-mst-01: The dosage shall at least have text or patient instructions