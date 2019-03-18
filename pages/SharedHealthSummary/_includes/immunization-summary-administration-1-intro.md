#### Summary Statement of Administered Vaccine *[[Draft](http://hl7.org/fhir/stu3/versions.html#maturity)]*

##### Usage scenarios

The following are the usage scenarios expected:

* Details of a vaccine administration exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


##### Implementation guidance

* Where additional content beyond that flagged with must c is provided it:
    * shall not qualify or negate content described by this profile as must support
    
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For the usage scenario for this profile it is expected that status will be ‘completed’


##### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

Sample instances are included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances:
* [Composition SHS example 2 (with contained resources)](Composition-bd06e981-ba86-4020-ba59-cd89f80e8712.html)

* [Composition SHS example 3 (with contained resources)](Composition-c53c6c39-3e1a-4038-9ad5-25be8c54481f.html)