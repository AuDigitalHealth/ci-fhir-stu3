#### Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#####  Implementation guidance 

##### PSML implementation guidance

For the expected usage scenarios in this implementation guide:

* Medication code from the [Australian Medication](https://healthterminologies.gov.au/fhir/ValueSet/australian-medication-1) value set is preffered.
* Where possible supply additional codes from the [PBSMedicinesItemCodes](http://build.fhir.org/ig/hl7au/au-fhir-base/ValueSet-pbs-item.html) value set.
* Either the active ingredient(s) or a brand name, or both, is expected to be included.
* The amount and strength of an active ingredient is expected to be included.
* For a medicine item with four or more active ingredients strength may be omitted.