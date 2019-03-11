This structure is derived from the STU3 FHIR<sup>&reg;</sup> resource [Explanation of Benefit](http://hl7.org/fhir/STU3/explanationofbenefit.html).

This profile introduces the following variations from the above core resource:
1.	Conditional invariants 
*	inv-dh-eob-01: A PBS or RPBS claim SHALL include a prescription.
*	inv-dh-eob-02: A MBS or DVABS claim SHALL NOT include a prescription.
*	inv-dh-eob-03: One of subType or item.category SHALL be present.
*   inv-dh-eob-04:  A PBS claim (subType='pbs') SHALL be of type 'Pharmacy' (type='pharmacy').
1. One `meta.profile` is 'http://ns.electronichealth.net.au/ci/fhir/StructureDefinition/explanationofbenefit-medicare'
1. Exactly one `identifier`
1.	`status` is 'active'
1.	`subType` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Australian Medicare Benefit and Claim Category](https://healthterminologies.gov.au/fhir/ValueSet/australian-medicare-benefit-claim-category-1) value set
1.	Exactly one `patient`
1.  `patient` as [AU Base Patient](http://www.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-patient.html)
1. Exactly one `created`
1.	`insurer` as [AU Base Organisation](http://www.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1.	`provider` as [AU Base Practitioner](http://fhir.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-practitioner.html)
1.	`organization` as [AU Base Organisation](http://www.hl7.org.au/fhir/base2018Sep/StructureDefinition-au-organisation.html)
1.	`referral` [contained](http://hl7.org/fhir/STU3/references.html#contained) as [Referral Request Medicare Benefits Schedule Department of Veterans’ Affairs](StructureDefinition-referralrequest-mbsdva.html)
1.	`prescription` [contained](http://hl7.org/fhir/STU3/references.html#contained) as [Medication Request Pharmaceutical Benefits Scheme](StructureDefinition-medicationrequest-pbs.html)
1.	Exactly one `item`
1. `item.sequence` is '1'
1.	`item.category` [extensible](http://hl7.org/fhir/STU3/terminologies.html#extensible) binding to [Australian Medicare Benefit and Claim Category](https://healthterminologies.gov.au/fhir/ValueSet/australian-medicare-benefit-claim-category-1) value set
1.	Exactly one `item.service` 
1. `item.service` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Australian Department of Human Services Modifications of Pharmaceutical Benefits Scheme Schedule Item, Medicare Benefits Schedule Item and Department of Veterans' Affairs Fee Schedule Item](https://healthterminologies.gov.au/fhir/ValueSet/australian-dhs-modifications-pbs-mbs-dva-item-1) value set
1.	Exactly one `item.serviced`






