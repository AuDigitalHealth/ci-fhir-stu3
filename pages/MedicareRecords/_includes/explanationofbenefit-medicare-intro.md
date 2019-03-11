This profile defines a representation of Pharmaceutical Benefits Schedule (PBS) claim items or Medicare Benefits Schedule (MBS) claim items. PBS claim items include information about pharmaceutical items prescribed and dispensed to an individual that were partially or fully funded under the PBS or Repatriation Pharmaceutical Benefits Scheme (RPBS). MBS claim items include information about healthcare services provided to an individual that were partially or fully funded by Medicare or the Department of Veterans' Affairs.

#####  **Usage Scenarios**
The following are the usage scenarios expected:
* DHS Medicare sends MBS records to the My Health Record system
* DHS Medicare sends PBS records to the My Health Record system

##### **Each Explanation of Benefit SHALL have**
1. a profile assertion to this profile
1. an identifier for this explanation of benefit record 
1. a patient
1. a creation date
1. an identification of the Medicare benefit (subtype or item.category)
1. an item that was claimed
1. a date of supply or service

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * status
    * type
    * subtype
    * created
    * provider
    * referral
    * prescription
    * item
    * item.sequence
    * item.category
    * item.service
    * item.serviced
    * item.quantity
* The system SHALL be able to take the following elements into account when performing processing:
    * identifier
    * patient
 
##### **Profile-specific implementation guidance**
* The patient resource should be identified in the patient element with a [logical reference](https://www.hl7.org/fhir/STU3/references.html#logical), i.e. an Australian IHI
* If a resource is referenced rather than identified in the applicable element, the referenced resource should be [contained](https://www.hl7.org/fhir/STU3/references.html#contained)
* PBS record: 
    * An ExplanationOfBenefit for a PBS record will represent prescription data as a MedicationRequest, including date of prescribing, number of repeats, and quantity
    * Generic name of a PBS item can be represented by the supplied item service code
    * Date of supply of the item is represented by item.serviced[x]
* MBS record: 
    * An ExplanationOfBenefit for an MBS record will represent the requester of the service as part of a ReferralRequest
    * Whether a service was provided in a hospital is indicated by the use and value of item.location
    * Date of service is represented by item.serviced[x]

#####  **Examples**
1. [Explanation of Benefit MBS example 1](ExplanationOfBenefit-explanationofbenefit-mbs-example-01.html)
1. [Explanation of Benefit MBS example 2](ExplanationOfBenefit-explanationofbenefit-mbs-example-02.html)
1. [Explanation of Benefit MBS example min](ExplanationOfBenefit-explanationofbenefit-mbs-example-min.html)
1. [Explanation of Benefit PBS example 1](ExplanationOfBenefit-explanationofbenefit-pbs-example-01.html)
1. [Explanation of Benefit PBS example 2](ExplanationOfBenefit-explanationofbenefit-pbs-example-02.html)


