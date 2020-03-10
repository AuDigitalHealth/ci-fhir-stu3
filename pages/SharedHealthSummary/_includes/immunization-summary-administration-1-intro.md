#### Summary Statement of Administered Vaccine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the expected usage scenarios in this implementation guide it is expected that:

* status will be ‘completed’.

* primarySource will be ‘true’.

* Where an authoring system does not have the dose status available as a distinct element it is expected that Dose Status Not Available will be sent {"system":"http://hl7.org/fhir/v3/NullFlavor","code":"NAVU","display":"Not available"}.
 
This profile is referenced by [Shared Health Summary](StructureDefinition-composition-shs-1.html).
 