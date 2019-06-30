### Summary of an Encounter for an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios
* A summary of an encounter between a patient and a healthcare provider exchanged as a referenced entry.

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profile.


##### Implementation guidance

For the supported scenarios in this implementation guide:

* It is expected that the status will be 'finished'. 
* The following elements are not expected to be provided but are encouraged if the sending system has this capability:
  * class
  * type
  * reason
* If provided, type is expected to support categorisation of the event from which the medicines list was generated, for example a code indicating a 'home medicines review' or 'pharmacist medicines review'.
* Period is expected to be equal to or prior to the Composition date and the List date.

When a shared medicines list is a PSML

* TBD (type)


