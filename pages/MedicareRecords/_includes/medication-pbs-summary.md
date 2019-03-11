This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [Medication](http://hl7.org/fhir/STU3/medication.html).

This profile introduces the following variations from the above core resource:
1. Exactly one `code`
1. `code` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Australian Department of Human Services Modified Pharmaceutical Benefits Scheme Schedule Item](https://healthterminologies.gov.au/fhir/ValueSet/australian-dhs-modified-pbs-item-1) value set
1. `manufacturer` as [AU Base Organisation](http://www.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)

