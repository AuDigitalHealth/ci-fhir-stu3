### Summary Statement of Known Procedure *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
The following are the usage scenarios expected:

* A summary statement for a procedure exchanged as referenced entry in a composition.

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 

#### Implementation guidance

* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For the usage scenario for this profile it is expected that status will be ‘completed’.

#### Examples
This section provides examples that conform to the requirements specified within this implementation guide.
* [Procedure example 1](Procedure-3bc4a0f3-1d3e-4bde-83a9-7a04dd5f4a77.html)

Sample instances are included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances. 
* [Composition SHS example 1 (with contained resources)](Composition-a0da969a-7956-439b-b390-8de071a2df7c.html)
