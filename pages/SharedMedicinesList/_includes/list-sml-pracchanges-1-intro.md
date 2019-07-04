### List of Medicine Items with Change Information Authored by Practitioner *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

The following are the overarching usage scenarios this profile is intended to support:
* A clinical information system (CIS) sends or receives a practitioner authored shared medicines list with the My Health Record system
* A contracted service provider (CSP) sends or receives a practitioner authored shared medicines list with the My Health Record system
* A CIS sends or receives a practitioner authored shared medicines list with another CIS or CSP
* A CSP sends or receives a practitioner authored shared medicines list with a CIS or another CSP
* A registered portal or registered repository receives a practitioner authored shared medicines list

An expected usage scenario, further scoping the above overarching scenarios is:
* A practitioner authored shared medicines list exchanged as a pharmacist shared medicines list (PSML) document 

This profile does not support sending an absence of clinical information as a list, e.g. no medicines information available.

##### Implementation guidance

For the supported scenarios in this implementation guide:

* All medicine items considered relevant by the practitioner preparing the list (the source) should be included in the list:
  * A new medicine item should be represented with the flag of ‘new’ or ‘prescribed’ and a change description that described the reason for introducing the medicine item.
  * An existing unchanged medicine item should be represented with the flag of ‘nochange’ and no change description.
  * An existing changed medicine item should be represented with the flag of ‘amended’ and a change description that describes the change, e.g. dose, form, route, frequency change.
  * A ceased medicine item should be represented with the flag of ‘ceased’ and a change description that describes the reason for ceasing the medicine item.
  * A withheld medicine item should be represented with the flag of ‘suspended’ and a change description supplied that describes reason for withholding the medicine, expected restart date or request for a clinical review.


##### When a shared medicines list is part of a document

When a shared medicines list is sent as part of a document (referenced in Composition.section.entry) rather than as a standalone resource the following guidance applies:

<table class="list" width="100%">
  <tr>
    <th>Element</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>author-role</td>
        <td>Will reference the same PractitionerRole as in Composition.composition-author-role</td>
    </tr>
   <tr>
        <td>subject</td>
        <td>Will reference the same Patient as in Composition.subject</td>
    </tr>   
   <tr>
        <td>date</td>
        <td>Will hold the same value as Composition.date</td>
    </tr>   
   <tr>
        <td>source</td>
        <td>Will reference the same Practitioner as in Composition.author</td>
    </tr>    
       <tr>
        <td>title</td>
        <td>Will not be provided</td>
    </tr>  
  </table> 


##### When a shared medicines list is a PSML

For the expected usage scenario of a PSML document the following guidance applies:

* The author will be a pharmacist and as such information relating to the pharmacist such as contact details will be recorded in the author as one more more elements of Practitioner.
* The role of ‘pharmacist’ will be recorded in the list source role as PractitionerRole.code.
* Encounter details, such as encounter type and period, are expected to be provided.
* All medicines that the patient is known to be taking, including packed, non-packed, complementary and over the counter medicine items, are expected to be included in the list.
* The list is expected to include at least one medicine item that the patient is known to be taking, i.e. the flag is not 'ceased'.
* The list may include relevant ceased medicine items for the patient.
* The list is not expected to include prescribed medicine items and change recommendations for the existing medicine items; the flag is never expected to have one of thes values: 'presribed',  'new-recommended', 'prescription-recommended', 'review-recommended', 'cessation-recommended', 'suspension-recommended' and 'cancellation-recommended'. 



