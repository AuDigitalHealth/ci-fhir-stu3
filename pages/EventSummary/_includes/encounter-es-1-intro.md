## **Summary of an Encounter for an Event**

The purpose of this profile is to provide a summary of an encounter, with a narrative description of the encounter, for an event between a patient and a healthcare provider. The description may capture text about the encounter that is not captured in other fields and include a summary of the issues or problems, management strategies, outcomes or progress, possible prognosis, and the patient’s understanding of the healthcare event.

##### **Usage Scenarios**
* A summary of an encounter between a patient and a healthcare provider exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.

##### **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

* The system SHALL be able to store and retrieve the following elements:
    * encounterDescription
    * status
    * period
    * reason
* The system SHALL be able to take the following elements into account when performing processing:
    * subject

##### **Profile specific implementation guidance**
* Where additional content beyond that flagged with a must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For the usage scenarios for this profile it is expected that the status will be 'finished'. 
