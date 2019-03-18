#### Base Patient *[[Draft](http://hl7.org/fhir/stu3/versions.html#maturity)]*

##### Usage scenarios
The following are the usage scenarios expected:

* Details of a patient exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 

##### Implementation guidance
* Medical Record Number: identifier.system can be completed using the [HPI-O based Medical Record Identifier](http://ns.electronichealth.net.au/id/local/provider/1.0) namespace if an organisation does not have its own namespace and has an HPI-O. An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/local/medicalrecord/1.0/8003620000000000". The dummy HPI-O should be replaced with the assigning entity's own HPI-O.


##### Known issues
* Due to a tolling issue the must support flag is missing for the below elements:
    * Patient.deceasedDateTime.date-accuracy-indicator

##### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

* [Patient example 1](Patient-e6e84607-a0da-4ead-9ed6-5e064fea9fc4.html)

Sample instances are also included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances:
* [Composition SHS example 1 (with contained resources)](Composition-a0da969a-7956-439b-b390-8de071a2df7c.html)

* [Composition SHS example 2 (with contained resources)](Composition-bd06e981-ba86-4020-ba59-cd89f80e8712.html)

* [Composition SHS example 3 (with contained resources)](Composition-c53c6c39-3e1a-4038-9ad5-25be8c54481f.html)