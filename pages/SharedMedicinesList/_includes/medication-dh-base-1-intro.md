#### Base Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#####  Implementation guidance 

For the overarching usage scenarios in this implementation guide:
* the medication code is preferred to be a member of the Australian Medication value set
* where the medication code identifies a branded medicine item, the expected text of code.text is the brand name and not the generic name

Where coding cannot be supplied and the medicine item is identified by:
* name but it is not known whether this is a brand or a generic name, the name is expected to be provided in only code.text
* by brand name only, the brand name is expected to be provided in code.text and optionally in brand name extension
* by generic name only, the generic name is expected to be provided in code.text and optionally in generic name extension
* by both brand and generic names, the brand name is expected to be provided in code.text and optionally in brand name extension, and the generic name is expected to be provided in the generic name extension

###### When a shared medicines list is a PSML
* where possible additional medication codes from the PBSMedicinesItemCodes value set should be supplied
