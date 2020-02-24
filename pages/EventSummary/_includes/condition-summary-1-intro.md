#### Summary Statement of Condition *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* verificationStatus will be ‘confirmed’
* the clinicalStatus will be ‘active’
* a ‘refuted’ condition will be represented with an appropriate negation code and a verificationStatus of ‘unconfirmed’ or ‘confirmed’ depending on the level of certainty
* a 'refuted' condition will be represented with an appropriate negation code and a clinicalStatus of ‘inactive’

This profile is referenced by [Event Summary](StructureDefinition-composition-es-1.html).
