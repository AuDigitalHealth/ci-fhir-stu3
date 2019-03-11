This profile contains the following variations from [AU Base Patient](http://hl7.org.au/fhir/StructureDefinition/au-patient):

* invariant: 
    * inv-dh-pat-03: The patient shall at least have an identifier or a name
* `name` as [Base HumanName](StructureDefinition-humanname-dh-base-1.html)
* `contact.relationship` [extensible](http://hl7.org/fhir/STU3/terminologies.html#extensible) binding to [Contact Relationship Type](https://healthterminologies.gov.au/fhir/ValueSet/contact-relationship-type-1)
* `contact.name` as [Base HumanName](StructureDefinition-humanname-dh-base-1.html)
* `contact.organization`  as [Base Organization](StructureDefinition-organization-dh-base-1.html)
* Zero (explicitly prohibited) `photo`
* Zero (explicitly prohibited) `animal`
* `generalPractitioner` as [Base Organization](StructureDefinition-organization-dh-base-1.html) | [Base Practitioner](StructureDefinition-practitioner-dh-base-1.html)
* `managingOrganization` as [Base Organization](StructureDefinition-organization-dh-base-1.html)

