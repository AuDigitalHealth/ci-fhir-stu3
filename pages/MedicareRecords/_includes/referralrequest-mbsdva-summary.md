This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [ReferralRequest](http://hl7.org/fhir/STU3/referralrequest.html).

This profile introduces the following variations from the above core resource:
1.	One `meta.profile` is 'http://ns.electronichealth.net.au/ci/fhir/StructureDefinition/referralrequest-mbsdva'
1. `status` is 'completed'
1.	`intent` is 'order'
1.	`subject` as [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html)
1.	Exactly one `requester`
1.  `requester.agent` as [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html)
1.	`requester.onBehalfOf` as [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1.	`speciality` [extensible](http://hl7.org/fhir/STU3/terminologies.html#extensible) binding to [Australian and New Zealand Standard Classification of Occupations](https://healthterminologies.gov.au/fhir/ValueSet/anzsco-1) value set
