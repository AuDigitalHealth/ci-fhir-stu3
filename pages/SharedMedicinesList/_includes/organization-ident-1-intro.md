#### Organization with Mandatory Identifier *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is recommended that:

* an Australian address conforms to [AU Base Address](https://hl7.org.au/fhir/base/aubase1.1/StructureDefinition-au-address.html)
* if more than one identifier is sent, only one of each type is sent

When sending a shared medicines list to the My Health Record system it is expected that:

* an HPI-O will be sent

This profile is referenced by [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html).
 