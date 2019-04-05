This profile defines a representation of a Personal Health Notes document for a patient in an Australian healthcare context. *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### **Usage Scenarios**
The following are the usage scenarios expected:
* An individual or their authorised representative authors a personal health notes document to be exchanged with the My Health Record system

##### **Profile-specific implementation guidance**
* For the usage scenarios for this profile it is required that the composition include only the specified top-level section; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.
* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content

