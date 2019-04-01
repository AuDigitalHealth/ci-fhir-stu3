### Summary Statement of Known Medication *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
The following are the usage scenarios expected:

* A statement of medication administration exchanged as referenced entry in a composition. 

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


#### Implementation guidance

* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For the usage scenario for this profile it is expected that status will be ‘active’.


#### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

* [MedicationStatement example 1](MedicationStatement/f7583f71-7736-4d10-89f7-fa1845e53120.html)
* [MedicationStatement example 2](MedicationStatement/314619c2-2d97-4fb9-9c25-b0b9da92f804.html)
* [MedicationStatement example 3](MedicationStatement/90d418aa-ed53-447b-95d2-099101ed4339.html)

Sample instances are included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances:
* [Composition SHS example 1 (with contained resources)](Composition-a0da969a-7956-439b-b390-8de071a2df7c.html)
* [Composition SHS example 3 (with contained resources)](Composition-c53c6c39-3e1a-4038-9ad5-25be8c54481f.html)
