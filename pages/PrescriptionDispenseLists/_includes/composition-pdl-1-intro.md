#### Prescription and / or Dispense List *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
The following are the overarching usage scenarios this profile is intended to support:
* A clinical information system (CIS) sends or receives
  * a prescription list as a document with the My Health Record system
  * a dispense record list as a document with the My Health Record system
  * a prescription and dispense record list as a document with the My Health Record system
* A contracted service provider (CSP) sends or receives
   * a prescription list as a document with the My Health Record system
   * a dispense record list as a document with the My Health Record system
   * a prescription and dispense record list as a document with the My Health Record system
* A CIS sends or receives
  * a prescription list as a document with another CIS or CSP
  * a dispense record list as a document with another CIS or CSP
  * a prescription and dispense record list as a document with another CIS or CSP
* A CSP sends or receives
  * a prescription list as a document with a CIS or another CSP
  * a dispense record list as a document with a CIS or another CSP
  * a prescription and dispense record list list as a document with a CIS or another CSP
* A registered portal or registered repository receives
    * a prescription list as a document
    * a dispense record list as a document
    * a prescription and dispense record list as a document 

An expected usage scenario, further scoping the above overarching scenarios is:
* Prescription and dispense view (PDV) exchanged with the My Health Record system

This profile does not support sending medicines change information (e.g. indicating cancellation or newly prescribed items) or event-specific information; in this case it is recommended that information is supplied as a shared medicines list.  

#### Implementation guidance
When the list is a prescription list it is expected that:
* code will be 57828-6 "Prescription list"
* one section of type Prescription List with the code 57828-6 "Prescription list" is expected
* a list entry will be sent
* if the list is generated from a filter or search query a provenance entry is expected

When the list is a dispense record list it is expected that:
* code will be 100.32014 "Dispense List"
* one section of type Dispense List with the code 100.32014 "Dispense List" is expected
* a list entry will be sent
* if the list is generated from a filter or search query a provenance entry is expected
 
When the list is a prescription and dispense list it is expected that:
* code will be 100.32015 "Prescription and Dispense List"
* section content will be supplied as either:
  * one section of type Prescription and Dispense List
  * two sections, one of type Dispense List and one of type Prescription List
* an empty section will be sent with an empty reason
* a non-empty section will be sent with a list entry
* if the list is generated from a filter or search query a provenance entry will be sent

Additionally when a prescription and dispense list is a PDV it is expected that:
* author will be the My Health Record system as a Device
* custodian will be the My Health Record system operator
* a non-empty section will be sent with a list entry and a provenance entry