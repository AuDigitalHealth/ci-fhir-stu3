## Summary Statement of Known Procedure

The purpose of this profile is to provide a summary statement for a known procedure.

#### Must Support
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements:
* status
* code
* subject
* performed
* note

#### Profile specific implementation guidance

* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For the usage scenario for this profile it is expected that status will be ‘completed’.
