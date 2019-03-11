This profile defines a representation of medication data to support representation of PBS claim items.

##### **Usage Scenarios**
The following are the usage scenarios expected:
* DHS Medicare sends PBS records to the My Health Record system

##### **Each Medication SHALL have**
1. a code identifying the medication

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * code
* The system SHALL be able to take the following elements into account when performing processing:
    * manufacturer

##### **Profile-specific implementation guidance**
* If a resource is referenced rather than identified in the applicable element, the referenced resource should be [contained](https://www.hl7.org/fhir/STU3/references.html#contained)

##### **Examples**
Sample instances are included within [Explanation of Benefit Medicare](StructureDefinition-explanationofbenefit-medicare.html) example instances. 