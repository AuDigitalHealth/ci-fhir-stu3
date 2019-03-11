This profile defines a representation of organ and tissue details to support representation of Australian Organ Donor Register records.

##### **Usage Scenarios**
The following are the usage scenarios expected:
* DHS Medicare sends Australian Organ Donor Register records to the My Health Record system

##### **Each BodySite SHALL have**
2.	a code identifying the organ or tissue
3.	a patient

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * code
* The system SHALL be able to take the following elements into account when performing processing:
    * patient

##### **Profile-specific implementation guidance**
* The patient resource should be identified in the patient element with a [logical reference](https://www.hl7.org/fhir/STU3/references.html#logical), i.e. an Australian IHI

##### **Examples**
Sample instances are included within [Consent Australian Organ Donor Register](StructureDefinition-consent-aodr.html) example instances.