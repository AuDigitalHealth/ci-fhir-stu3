#### Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#####  Implementation guidance 
For the supported scenarios in this implementation guide:

* Where the code identifies a branded medicine item, the name is expected to be provided in code.text. 
* Where the code identifies a generic medicine item, the name is expected to be provided in code.text.
* Where there is no code and a medicine item is identified by a brand name only, the name is expected to be provided in code.text and optionally in brand name extension. 
* Where there is no code and a medicine item is identified by a generic name only, the name is expected to be provided in code.text and optionally in generic name extension.
* Where there is no code and both brand and generic names are available, brand name in expected to be provided in code.text and optionally in brand name extension, and generic name is expected to be provided in the generic name extension.
* Where there is no code and it is unknown whether the medicine item name is a brand name or a generic name, the name is expected to be provided in code.text only.

When a shared medicines list is a PSML
* Medication code from the [Australian Medication](https://healthterminologies.gov.au/fhir/ValueSet/australian-medication-1) value set is preffered.
* Where possible supply additional codes from the [PBSMedicinesItemCodes](http://build.fhir.org/ig/hl7au/au-fhir-base/ValueSet-pbs-item.html) value set.
* Either the active ingredient(s) or a brand name, or both, is expected to be included.
* The amount and strength of an active ingredient is expected to be included.
* For a medicine item with four or more active ingredients strength may be omitted.