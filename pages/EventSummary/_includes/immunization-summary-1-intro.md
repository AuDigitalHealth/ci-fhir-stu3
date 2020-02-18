#### Summary Statement of Vaccine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* status will be ‘completed’
* primarySource will be ‘true’
* where an authoring system does not have the dose status available as a distinct element, Dose Status Not Available will be sent {"system":"http://hl7.org/fhir/v3/NullFlavor","code":"NAVU","display":"Not available"}

This profile is referenced by [Event Summary](StructureDefinition-composition-es-1.html)
