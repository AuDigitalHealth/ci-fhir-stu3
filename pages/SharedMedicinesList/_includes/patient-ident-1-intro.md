#### Patient with Mandatory Identifier *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is recommended that:
* an Australian address conforms to [AU Base Address](https://hl7.org.au/fhir/base/aubase1.1/StructureDefinition-au-address.html)

When sending a shared medicines list to the My Health Record system it is expected that:
* indigenous status will be sent
* an IHI will be sent
* gender will be sent
* birthDate will be sent
* address will not be sent
* telecom will not be sent