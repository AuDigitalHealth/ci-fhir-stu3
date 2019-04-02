#### Summary Statement of Administered Vaccine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios

The following are the usage scenarios expected:

* Details of a vaccine administration exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


##### Implementation guidance

* For the usage scenario for this profile, it is expected that status will be ‘completed’.
* For the usage scenario for this profile, it is expected that primarySource will be ‘true’.
* Where an authoring system does not have the dose status available as a distinct element it is expected that Dose Status Not Available will be sent {"system":"http://hl7.org/fhir/v3/NullFlavor","code":"NAVU","display":"Not available"}
