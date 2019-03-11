This profile defines a representation of vaccination information from the Australian Immunisation Register.

##### **Usage Scenarios**
 The following are the usage scenarios expected:
* DHS Medicare sends records of administered vaccines to the My Health Record system

##### **Each Immunization SHALL have**
1. a profile assertion to this profile
1. an identifier for this immunisation record
1. a status of vaccination event
1. a flag to indicate whether the vaccine was administered
1. a vaccine 
1. a patient
1. a flag to indicate this data is based on information from the person who administered the vaccine

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * status
    * notGiven
    * vaccineCode
    * date
    * primarySource
    * explanation
    * explanation.reasonNotGiven
    *  vaccinationProtocol
    * vaccinationProtocol.targetDisease
    * vaccinationProtocol.doseStatus
    * extension-immunization-cancellationperiod
* The system SHALL be able to take the following elements into account when performing processing:
    * identifier
    * patient

##### **Profile-specific implementation guidance**
* The patient resource should be identified in the patient element with a [logical reference](https://www.hl7.org/fhir/STU3/references.html#logical), i.e. an Australian IHI
* If a resource is referenced rather than identified in the applicable element, the referenced resource should be [contained](https://www.hl7.org/fhir/STU3/references.html#contained)
* In order to provide identification of a target disease to be protected against, the resource requires a dose status; this data is not available so doseStatus has been set to NAVU Not Available
* Though not expected to be provided, a cancelled, rejected, or not administered vaccination can be represented using notGiven=true and status=completed

##### **Examples**
1. [Administered immunisation - short](Immunization-immunization-air-example-administration-short.html)
1. [Administered immunisation](Immunization-immunization-air-example-administration.html)
1. [Immunisation not given](Immunization-immunization-air-example-notGiven.html)
1. [Administered immunisation with text list of targetDisease](Immunization-immunization-air-example-administration-text.html)



