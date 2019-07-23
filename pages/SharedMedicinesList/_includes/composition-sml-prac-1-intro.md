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

For the overarching usage scenarios in this implementation guide:

* Where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance is sent with the appropriate negation code (e.g. 716186003 |No known allergy|) is sent as the code in the Allergies section.
* Where a sending system can state that a patient is known not to have current medications it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234391000168107 |No known current medications|) in the Medications section.
* If a sending system has no clinical data for a particular section then section.emptyReason may be used.

For the expected usage scenario of a PSML document the following guidance applies:

* It is expected that status will be ‘final’.
* It is expected that author will be the person acting as the pharmacist, and composition author role is pharmacist
* It is expected that encounter will be sent
* It is expected that the Allergies section is only sent if there is one or more entries
* It is expected that the Medications section will contain a medication list entry



 
  
   
