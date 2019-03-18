This profile contains the following variations from [AU Base Condition](http://hl7.org.au/fhir/StructureDefinition/au-condition):

* `recorder` as [Base Patient](StructureDefinition-patient-dh-base-1.html), [Base Practitioner](StructureDefinition-practitioner-dh-base-1.html), [Base RelatedPerson](StructureDefinition-relatedperson-dh-base-1.html),
* Exactly one `code`
* `subject` as [Patient with Mandatory Identifier](StructureDefinition-patient-ident-1.html) 
* `onset[x]` as as [dateTime](http://hl7.org/fhir/STU3/datatypes.html#dateTime), [Age](http://hl7.org/fhir/STU3/datatypes.html#Age), [Period](http://hl7.org/fhir/STU3/datatypes.html#Period), [Range](http://hl7.org/fhir/STU3/datatypes.html#Range)
* `abatement[x]` as [dateTime](http://hl7.org/fhir/STU3/datatypes.html#dateTime), [Age](http://hl7.org/fhir/STU3/datatypes.html#Age), [boolean](http://hl7.org/fhir/STU3/datatypes.html#boolean), [Period](http://hl7.org/fhir/STU3/datatypes.html#Period), [Range](http://hl7.org/fhir/STU3/datatypes.html#Range)