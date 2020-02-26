#### Summary of an Encounter for an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
* A summary of an encounter between a patient and a healthcare provider exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.


#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* status will be 'finished' 
* the following elements are not likely to be sent but are encouraged:
  * class
  * reason
* period is equal to, or prior to, Composition date and List date

This profile is referenced by [Event Summary](StructureDefinition-composition-es-1.html).
