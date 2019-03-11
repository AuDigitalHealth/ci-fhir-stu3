This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [BodySite](http://hl7.org/fhir/STU3/bodysite.html).

This profile introduces the following variations from the above core resource:
1. Exactly one `code`
1. `code` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Organ Donation Body Site](https://healthterminologies.gov.au/fhir/ValueSet/organ-donation-body-site-1) value set
1. `patient` as [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html)
