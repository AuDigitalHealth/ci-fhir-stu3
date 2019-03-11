This profile defines a representation of the practitioner that requested the service to support representation of Medicare Benefits Schedule (MBS) claim item records.

#####  **Usage Scenarios**
The following are the usage scenarios expected:
* DHS Medicare sends MBS records to the My Health Record system

##### **Each ReferralRequest SHALL have**
1. a profile assertion to this profile 
1. a status of referral request
1. an intent
1. a patient
1. a practitioner that requested the service

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * status
    * intent
    * requester
    * requester.agent
    * requester.onBehalfOf
    * specialty
* The system SHALL be able to take the following elements into account when performing processing:
   * identifier
    * subject

##### **Profile-specific implementation guidance**
* The patient resource should be identified in the subject element with a [logical reference](https://www.hl7.org/fhir/STU3/references.html#logical), i.e. an Australian IHI
* If a resource is referenced rather than identified in the applicable element, the referenced resource should be [contained](https://www.hl7.org/fhir/STU3/references.html#contained)

#####  **Examples**
Sample instances are included within [Explanation of Benefit Medicare](StructureDefinition-explanationofbenefit-medicare.html) example instances. 