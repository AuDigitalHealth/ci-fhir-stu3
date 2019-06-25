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


##### When a shared medicines list is a PSML

* The role of ‘pharmacist’ will be recorded in the composition author role as PractitionerRole.code.
* Information relating to the pharmacist such as contact details will be recorded in the author as one more more elements of Practitioner.
* In the Medications section, a medication list entry is always expected to be provided.



 
  
   
