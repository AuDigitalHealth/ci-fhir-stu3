#### Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#####  Implementation guidance 

* Where the code identifies a branded medicine item, brand name is expected to be provided in code.text and optionally in brand name extension. 
* Where the code identifies a generic medicine item, generic name is expected to be provided in code.text and optionally in generic name extension.
* When a medicine item is identified by a brand name only, the name is expected to be provided in code.text and optionally in brand name extension. 
* When a medicine item is identified by a generic name only, the name is expected to be provided in code.text and optionally in generic name extension.
* When both brand and generic names are available, brand name in expected to be provided in code.text and optionally in brand name extension, and generic name is expected to be provided in the generic name extension.
* When it is unknown if the medicine item name is a brand or a generic name, the name is expected to be provided in code.text only.

##### PSML implementation guidance

For the expected usage scenarios in this implementation guide:

* Medication code from the [Australian Medication](https://healthterminologies.gov.au/fhir/ValueSet/australian-medication-1) value set is preffered.
* Where possible supply additional codes from the [PBSMedicinesItemCodes](http://build.fhir.org/ig/hl7au/au-fhir-base/ValueSet-pbs-item.html) value set.
* Either the active ingredient(s) or a brand name, or both, is expected to be included.
* The amount and strength of an active ingredient is expected to be included.
* For a medicine item with four or more active ingredients strength may be omitted.