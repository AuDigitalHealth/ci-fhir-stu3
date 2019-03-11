This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [MedicationRequest](http://hl7.org/fhir/STU3/medicationrequest.html).

This profile introduces the following variations from the above core resource:
1. One `meta.profile` is 'http://ns.electronichealth.net.au/ci/fhir/StructureDefinition/medicationrequest-pbs'
1. `intent` is 'order'
1. `medication` as `medicationReference`
1. `medicationReference` [contained](http://hl7.org/fhir/STU3/references.html#contained) as [Medication Pharmaceutical Benefits Scheme](StructureDefinition-medication-pbs.html)
1. `subject` as [AU Base Patient](http://www.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html)
1. Exactly one `authoredOn`
1. `requester.agent` as [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html), [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1. Exactly one `dispenseRequest`
1. Exactly one `dispenseRequest.quantity`
1. `dispenseRequest.performer` as [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)


