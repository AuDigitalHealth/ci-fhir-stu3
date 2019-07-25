#### PractitionerRole with Practitioner with Mandatory Identifier *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the expected usage scenario of a PSML document the following guidance applies:

* The role of ‘pharmacist’ will be recorded in the composition author role as PractitionerRole.code.
* The PractitionerRole.practitioner will be a pharmacist and as such information relating to the pharmacist such as contact details will be recorded in the referenced Practitioner as one more more elements of Practitioner.
* Availability information (availableTime, notAvailable, and availabilityExceptions) are not expected

