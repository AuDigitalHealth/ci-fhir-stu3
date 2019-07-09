#### Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#####  Implementation guidance 
For the supported scenarios in this implementation guide:
* Medication code from the [Australian Medication](https://healthterminologies.gov.au/fhir/ValueSet/australian-medication-1) value set is preferred.
* Where possible additional codes from the [PBSMedicinesItemCodes](http://build.fhir.org/ig/hl7au/au-fhir-base/ValueSet-pbs-item.html) value set are expected to be supplied.
* Where the medication code identifies a branded medicine item, the brand name may also be provided in code.text. 
* Where the medication code identifies a generic medicine item, the generic name may also be provided in code.text.
* Where a medication item is identified by a brand name only (and not by medication code), the brand name is expected to be provided in code.text and optionally in brand name extension. 
* Where a medicine item is identified by a generic name only (and not by medication code), the generic name is expected to be provided in code.text and optionally in generic name extension.
* Where both brand and generic names for a medicine item are available (and no medication code), the brand name in expected to be provided in code.text and optionally in brand name extension, and the generic name is expected to be provided in the generic name extension.
* Where a medicine item is identified by a name only (and not by medication code), and is unknown whether this is a brand or a generic name, the name is expected to be provided in code.text only.

