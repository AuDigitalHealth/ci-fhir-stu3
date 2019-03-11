This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [Immunization](http://hl7.org/fhir/STU3/immunization.html).

This profile introduces the following variations from the above core resource:
1.	Conditional invariants
*	inv-dh-imm-01: If immunization was administered (notGiven is false) then date SHALL be present and cancellation period SHALL be absent.
1.	One `meta.profile` is 'http://ns.electronichealth.net.au/ci/fhir/StructureDefinition/immunization-air'
1. Exactly one `identifier`
1. `status` is 'completed'
1.	`vaccineCode` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Australian Vaccine](https://healthterminologies.gov.au/fhir/ValueSet/australian-vaccine-1) value set
1.	`patient` as [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html)
1. `primarySource` is 'true'
1.	`manufacturer` as [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1.	`practitioner.actor` as [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html)
1.	`explanation.reasonNotGiven` [extensible](http://hl7.org/fhir/STU3/terminologies.html#extensible) binding to [Reason Vaccine Not Administered](https://healthterminologies.gov.au/fhir/ValueSet/reason-vaccine-not-administered-1) value set
1. At most one `vaccinationProtocol`
1. `vaccinationProtocol.authority` as [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1.	`vaccinationProtocol.doseStatus` is Not available (Details : {[http://hl7.org/fhir/v3/NullFlavor](http://hl7.org/fhir/v3/NullFlavor/cs.html) code 'NAVU'})
1.	At most one [Extension Immunization Cancellation Period ](StructureDefinition-extension-immunization-cancellationperiod.html)










