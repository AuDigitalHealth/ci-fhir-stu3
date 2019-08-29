#### List of Medicine Items with Change Information Authored by Practitioner *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

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

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that a list:

* will be sent with all medicine items considered relevant by the practitioner preparing the list (the source) should be included in the list including packed, non-packed, complementary and over the counter medicine items
* with a List.code of '101.32027' Ceased Medicines will be sent with only ceased medicine items
* with a List.code of '101.32009' Current Medicines will be sent with new or existing medicine items and no ceased medicine items

<table class="list" width="100%">
  <tr>
    <th>Item</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>new medicine item</td>
        <td>Will be represented with the flag of ‘new’ or ‘prescribed’ and a change description that described the reason for introducing the medicine item</td>
    </tr>
         <tr>
        <td>existing unchanged medicine item</td>
        <td>Will be represented with the flag of ‘nochange’ and no change description</td>
    </tr>
    <tr>
        <td>existing changed medicine item</td>
        <td>Will be represented with the flag of ‘amended’ and a change description that describes the change, e.g. dose, form, route, frequency change</td>
    </tr>
    <tr>
        <td>ceased medicine item</td>
        <td>Will be represented with the flag of ‘ceased’ and a change description that describes the reason for ceasing the medicine item</td>
    </tr>
        <tr>
        <td>withheld medicine item</td>
        <td>Will be represented with the flag of ‘suspended’ and a change description supplied that describes reason for withholding the medicine, expected restart date or request for a clinical review</td>
    </tr>
    </table>

When a shared medicines list is sent as part of a document (referenced in Composition.section.entry) rather than as a standalone resource the guidance in the following table applies.

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
        <td>code</td>
        <td>Will hold the same value as Composition.section(Medicines list).code</td>
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
        <td>Not to be sent</td>
    </tr>  
  </table> 

Additionally, when the shared medicines list is a PSML document it is expected that:

* if the list has a List.code of '10160–0' History of Medication use Narrative, it will be sent with at least one new or existing medicine item
* encounter will be sent
* where a sending system can state that one or more medicine items are packed by a pharmacy in a dose administration aid, the preferred text 'Packed medicines: Yes', 'Packed medicines: No', or 'Packed medicines: Unknown' will be sent in note
* list items will not include:
  * recommendations (flag is not to be 'new-recommended', 'prescription-recommended', 'review-recommended', 'cessation-recommended', 'suspension-recommended' and 'cancellation-recommended')
  * prescribed medicine items (flag is not to be ‘prescribed’)