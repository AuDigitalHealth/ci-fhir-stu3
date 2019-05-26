### List of Medicine Items for a Patient *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

The following are the overarching usage scenarios this profile is intended to support:
* A clinical information system (CIS) sends or receives a shared medicines list with the My Health Record system
* A contracted service provider (CSP) sends or receives a shared medicines list with the My Health Record system
* A CIS sends or receives a shared medicines list with another CIS or CSP
* A CSP sends or receives a shared medicines list with a CIS or another CSP
* A registered portal or registered repository receives a shared medicines list

An expected usage scenario, further scoping the above overarching scenarios is:
* A shared medicines list exchanged as a pharmacist shared medicines list (PSML) document 


##### Implementation guidance

For the supported scenarios in this implementation guide:

* Where a sending system wants to include information that cannot be directly included in a supported list entry resource, the information may be included via a resource that is referenced from the supported list entries
* All medicine items considered relevant by the practitioner preparing the list (the source) should be included in the list:
* A new medicine item should be represented with the flag of ‘new’ or ‘prescribed’ and a change description that described the reason for introducing the medicine item.
* An existing unchanged medicine item should be represented with the flag of ‘nochange’ and no change description.
* A changed medicine item should be represented with the flag of ‘amended’ and a change description that describes the change, e.g. dose, form, route, frequency change.
* A ceased medicine item should be represented with the flag of ‘ceased’ and a change description that describes the reason for ceasing the medicine item.
* A withheld medicine item should be represented with the flag of ‘suspended’ and a change-description supplied that describes reason for withholding the medicine, expected restart date or request for a clinical review.


##### When a shared medicines list is part of a document

When a shared medicines list is sent as part of a document (referenced in Composition.section.entry) rather than as a standalone resource the following guidance applies:

<table class="list" width="100%">
  <tr>
    <th>Element</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>list source role</td>
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
* The role of ‘pharmacist’ will be recorded in the list source role as PractitionerRole.code
* Information relating to the pharmacist such as contact details will be recorded in the source as one more more elements of Practitioner
* All medicines that the patient is known to be taking, including packed, non-packed, complementary and over the counter medicine items, are expected to be included in the list.
* Relevant ceased medicine items for the patient may be included in the list.



