### Base Medication *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance 

For the overarching usage scenarios in this implementation guide it is recommended that:

* Medication.code is a member of the [Australian Medication](https://healthterminologies.gov.au/fhir/ValueSet/australian-medication-1) value set
* where Medication.code is a branded medicine item, Medication.code.text is the branded name

Where a sending system cannot send a coded value (only Medication.code.text can be supplied) it is expected that:

* if both brand name and generic name can be sent, brand name will be sent in Medication.code.text and optionally in brand name extension, and generic name will be sent in the generic name extension
* if only brand name can be sent, brand name will be sent in Medication.code.text and optionally in the brand name extension
* if only generic name can be sent, generic name will be sent in Medication.code.text and optionally in the generic name extension
* if a name can be sent, but it cannot be determined if it is a brand or generic name, the name will be sent only in Medication.code.text

Additionally, when the shared medicines list is a PSML document it is expected that:

* Medication.code will also be sent with additional codes that are members of the PBS Item code system ([http://pbs.gov.au/code/item](http://pbs.gov.au/code/item))