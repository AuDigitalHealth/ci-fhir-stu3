### List of Medicine Changes from an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

* A medicine list exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.

#### Implementation guidance

For the expected usage scenarios in this implementation guide:

* Where date is provided, it is expected to be the same as the date of the referencing Composition.

* Where source is provided, it is expected to be the same as the author of the referencing Composition.

* All medicine items relevant to an event should be included in the list:

    * For existing unchanged medicine items, the flag  will be 'unchanged' and change description is not expected to be provided.

    * For new and changed medicine items, change description is expected to be provided.

