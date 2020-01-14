#### PractitionerRole with Practitioner with Mandatory Identifier *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

No additional guidance is suggested to support implementation of this profile for the overarching usage scenarios this implementation guide is intended to support.

When the shared medicines list is a PSML document it is expected that:

* PractitionerRole.code will be a value equivalent to the author's professional role, e.g. 159011008 \|Community pharmacist\|
* practitioner will be sent as a reference to a Practitioner resource for the author, e.g. the pharmacist
* the organisation the author is representing (PractitionerRole.organization), e.g. pharmacy, will be sent as a reference to an Organization resource
* availability information (availableTime, notAvailable, and availabilityExceptions) will not be sent