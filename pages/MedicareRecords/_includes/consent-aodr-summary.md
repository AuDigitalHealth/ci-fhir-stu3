This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [Consent](http://hl7.org/fhir/STU3/consent.html).

This profile introduces the following variations from the above core resource:
1. Conditional invariants
* inv-dh-cons-01: If donation decision is 'permit', there SHALL be a specific organ (except.data.reference).
* inv-dh-cons-02: If donation decision is 'deny', there SHALL NOT be a specific organ (except.data.reference).
1. One `meta.profile` is 'http://ns.electronichealth.net.au/ci/fhir/StructureDefinition/consent-aodr'
1. Exactly one `identifier`
1. `status` is 'active'
1. One `category` is Organ donation consent (Details : {LOINC code '64300-7'})
1. `patient` as [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html)
1. Exactly one `dateTime`
1. `consentingParty` as [RelatedPerson](http://hl7.org/fhir/STU3/relatedperson.html), [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html), [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html), [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html)
1. `actor.reference` as [AU Base Device](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-device.html),[Group](http://hl7.org/fhir/STU3/group.html), [CareTeam](http://hl7.org/fhir/STU3/careteam.html), [RelatedPerson](http://hl7.org/fhir/STU3/relatedperson.html), [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html), [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html), [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html)
1. `organization` as [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1. Exactly one `policy`
1. `policy.authority` is 'http://australianorgandonorregister.gov.au'
1. Exactly one `policy.uri`
1. `policy.uri` is 'http://www.australianorgandonorregister.gov.au/aodr'
1. `except.actor.reference` as [AU Base Device](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-device.html), [Group](http://hl7.org/fhir/STU3/group.html), [CareTeam](http://hl7.org/fhir/STU3/careteam.html), [RelatedPerson](http://hl7.org/fhir/STU3/relatedperson.html), [AU Base Organisation](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html), [AU Base Patient](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html), [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html)   
1. Exactly one `except.action`
1. `except.action` is Harvesting of donor material (Details : {SNOMED CT code '53958007'})
1. Exactly one `except.data`
1. `except.data.meaning` is 'instance'
1. `except.data.reference` [contained](https://www.hl7.org/fhir/STU3/references.html#contained) as [BodySite Australian Organ Donor Register](StructureDefinition-bodysite-aodr.html) 
1. At most one [Extension Date Initial Registration](StructureDefinition-extension-dateinitialregistration.html)
1. Exactly one [Extension Consent Donation Decision](StructureDefinition-extension-donationdecision.html)
