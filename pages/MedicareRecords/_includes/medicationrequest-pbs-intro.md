This profile defines a representation of prescription data to support representation of PBS claim items.

#####  **Usage Scenarios**
The following are the usage scenarios expected:
* DHS Medicare sends PBS records to the My Health Record system

##### **Each MedicationRequest SHALL have**
1.	a profile assertion to this profile 
2.	an intent
3.	a medication
4.	a patient
5.	a date of prescribing
6.	a number of repeats allowed
6.  an amount of medication per dispense 

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * status
    * intent
    * medication
    * authoredOn
    * dispeseRequest
    * dispenseRequest.numberOfRepeatsAllowed
    * dispeseRequest.quantity
* The system SHALL be able to take the following elements into account when performing processing:
    * identifier
    * subject

##### **Profile-specific implementation guidance**
* The patient resource should be identified in the subject element with a [logical reference](https://www.hl7.org/fhir/STU3/references.html#logical), i.e. an Australian IHI
* If a resource is referenced rather than identified in the applicable element, the referenced resource should be [contained](https://www.hl7.org/fhir/STU3/references.html#contained)
* The referenced medication resource will include the code for the medication and the manufacturer if known
* If the number of permitted repeats for a prescription are zero, the numberOfRepeatsAllowed element should not be included - the value of '0' cannot be used

##### **Examples**
Sample instances are included within [Explanation of Benefit Medicare](StructureDefinition-explanationofbenefit-medicare.html) example instances. 