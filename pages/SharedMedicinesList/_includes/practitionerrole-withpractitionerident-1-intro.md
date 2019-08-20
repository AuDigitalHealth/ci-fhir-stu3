#### PractitionerRole with Practitioner with Mandatory Identifier *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

No additional guidance is suggested to support implementation of this profile for the overarching usage scenarios this implementation guide is intended to support.

For the expected usage scenario of a PSML document the following guidance applies:

* a code equivalent to pharmacist will be sent
* the practitioner will be a reference to a Practitioner resource that includes information relating to the pharmacist such as contact details
* availability information (availableTime, notAvailable, and availabilityExceptions) will not be sent
