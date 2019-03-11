This profile defines a representation of donation decision information from the Australian Organ Donor Register.

##### **Usage Scenarios**
The following are the usage scenarios expected:
* DHS Medicare sends Australian Organ Donor Register records to the My Health Record system

##### **Each Consent SHALL have**
1. a profile assertion to this profile
1. an identifier for this consent record
1. a status of consent record 
1. a category of organ donation consent
1. a patient
1. a creation date
1. an identification that the consent is to the Australian Organ Donor Register policy (policy.uri)
1. a decision of whether or not the individual consents to be an organ donor

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * status
    * category
    * dateTime
    * policy
    * policy.authority
    * policy.uri
    * except
    * except.type
    * except.action
    * except.data
    * except.data.reference
    * extension-dateinitialregistration
    * extension-donationdecision
* The system SHALL be able to take the following elements into account when performing processing:
    * identifier
    * patient

##### **Profile-specific implementation guidance**
* The patient resource should be identified in the patient element with a [logical reference](https://www.hl7.org/fhir/STU3/references.html#logical), i.e. an Australian IHI
* If a resource is referenced rather than identified in the applicable element, the referenced resource should be [contained](https://www.hl7.org/fhir/STU3/references.html#contained)
* One instance of category is fixed to Organ donation consent LOINC code “64300-7”, other meaningful category codes can also be supplied
* An individual's decision not to be a donor is represented by the extension Donation Decision with the SNOMED CT code 161034004 &#124;*Not willing to be a donor*&#124;
* An individual's decision to be a donor is represented by:
    * the extension Donation Decision with SNOMED CT code 160654005 &#124;*Willing to be donor*&#124;
    * listing a decision (permit or deny) for each specific organ and tissue that can be donated, each of which is represented by an except structure referencing a BodySite resource

##### **Examples**

1. [Willing to donate](Consent-aodr-example-willingtodonate.html)
1. [Willing to donate some](Consent-aodr-example-willingtodonatesome.html)
1. [Not willing to donate](Consent-aodr-example-notwillingtodonate.html)



