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


##### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

* [Condition example 1](Condition-b021320c-bc5e-4ae8-b9fc-1ed2d876e889.html)

* [Condition example 2](Condition-cfa41daf-b5a6-4a05-9166-a4b7c23f08a1.html)

Sample instances are also included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances:
* [Composition SHS example 1 (with contained resources)](Composition-a0da969a-7956-439b-b390-8de071a2df7c.html)


