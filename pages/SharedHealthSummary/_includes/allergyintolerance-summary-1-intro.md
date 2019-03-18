#### Summary Statement of Allergy or Intolerance *[[Draft](http://hl7.org/fhir/stu3/versions.html#maturity)]*

##### Usage scenarios

The following are the usage scenarios expected:

* A summary statement for an allergy or intolerance exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


##### Implementation guidance
* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
   
   * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content

* If an authoring system only has substance or agent available and not a statement of allergy intolerance that substance should be recorded in the code and optionally reaction.substance.

* For the usage scenario for this profile it is expected that verificationStatus will be ‘unconfirmed’ (where a sending system does not clearly have this element this should be the value sent), but may be ‘confirmed’. A ‘refuted’ allergy should be represented with an appropriate negation code.

*  For the usage scenarios for this profile it is expected that the clinicalStatus will be ‘active’.


##### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

* [AllergyIntolerance example 1](AllergyIntolerance-a5e03840-1be4-43e0-acd2-c9e288adc4f9.html)

Sample instances are also included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances:
* [Composition SHS example 1 (with contained resources)](Composition-a0da969a-7956-439b-b390-8de071a2df7c.html)

* [Composition SHS example 2 (with contained resources)](Composition-bd06e981-ba86-4020-ba59-cd89f80e8712.html)

* [Composition SHS example 3 (with contained resources)](Composition-c53c6c39-3e1a-4038-9ad5-25be8c54481f.html)