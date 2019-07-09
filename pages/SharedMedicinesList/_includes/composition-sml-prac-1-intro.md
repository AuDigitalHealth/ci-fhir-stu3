#### Shared Medicines List Authored by Practitioner *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios 

The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) sends or receives a practitioner authored shared medicines list document with the My Health Record system
* A contracted service provider (CSP) sends or receives a practitioner authored shared medicines list document with the My Health Record system
* A CIS sends or receives a practitioner authored shared medicines list document with another CIS or CSP
* A CSP sends or receives a practitioner authored shared medicines list document with a CIS or another CSP
* A registered portal or registered repository receives a practitioner authored shared medicines list document

An expected usage scenario, further scoping the above overarching scenarios is:
* A practitioner authored shared medicines list document exchanged as a pharmacist shared medicines list (PSML)

#####  Implementation guidance 

For the supported scenarios in this implementation guide:

* In the Allergies section, where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance is sent with the appropriate negation code (e.g. 716186003 \|No known allergy\|) is sent as the code.
* In the Allergies section, where a sending system does not have any clinical data to provide it is expected that section.emptyReason is used.
* In the Medications section, where a sending system can state that a patient is known not to have current medications it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234391000168107 \|No known current medications\|) 
* In the Medications section, where a sending system does not have any clinical data to provide it is expected that section.emptyReason is used.

##### When a shared medicines list is a PSML

* It is expected that status will be ‘final’.
* The author will be a pharmacist and as such information relating to the pharmacist such as contact details will be recorded in the author as one more more elements of Practitioner.
* The role of ‘pharmacist’ will be recorded in the composition author role as PractitionerRole.code.
* Encounter details, such as encounter type and period, are expected to be provided.
* Allergies section is only expected to be provided when a clinical system has data relating allergy or category of allergies.
* In the Medications section, a medicines list entry is always expected to be provided.



 
  
   
