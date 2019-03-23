#### Summary Statement of Condition *[[Draft](http://hl7.org/fhir/stu3/versions.html#maturity)]*

##### Usage scenarios

The following are the usage scenarios expected:

* A summary statement of a condition, problem or diagnosis exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 



##### Implementation guidance
* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
    
* For the usage scenario for this profile it is expected that status will be ‘active’.

* For the usage scenario for this profile it is expected that verificationStatus will be ‘unknown’. Where a sending system does not clearly have this element this should be the value sent.



