#### Summary Statement of Known Procedure *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios
The following are the usage scenarios expected:

* A summary statement for a procedure exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 

##### Implementation guidance

* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
    
* For the usage scenario for this profile it is expected that status will be ‘completed’.


