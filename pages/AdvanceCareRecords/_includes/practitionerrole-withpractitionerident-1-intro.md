#### PractitionerRole with Practitioner with Mandatory Identifier *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is recommended that:
* PractitionerRole.code will be a value equivalent to the author's professional role, e.g. General Practitioner
* practitioner will be sent as a reference to a Practitioner resource for the author
* the organisation the author is representing (PractitionerRole.organization), e.g. family clinic, will be sent as a reference to an Organization resource
* availability information (availableTime, notAvailable, and availabilityExceptions) will not be sent

This profile is referenced by [Advance Care Directive Custodian Record](StructureDefinition-composition-acdcr-1.html), [Advance Care Planning](StructureDefinition-composition-acp-1.html) and [Advance Care Planning Document Reference](StructureDefinition-documentreference-acp-1.html).