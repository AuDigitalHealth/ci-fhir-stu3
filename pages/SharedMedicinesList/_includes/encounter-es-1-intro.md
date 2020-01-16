#### Summary of an Encounter for an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* status will be 'finished' 
* the following elements are not likely to be sent but are encouraged:
  * class
  * reason
* type will support categorisation of the event from which the medicines list was generated, for example a code indicating a home medicines review
* period is equal to, or prior to, Composition date and List date

When the shared medicines list is a PSML document, it is expected that type will have a code from [Medicines Review Type](https://healthterminologies.gov.au/fhir/ValueSet/medicines-review-type-2).

This profile is referenced by [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html), 
[List of Medicine Items with Change Information Authored by Practitioner](StructureDefinition-list-sml-pracchanges-1.html), 
and [Medicine Item Statement](StructureDefinition-medicationstatement-detailed-1.html).