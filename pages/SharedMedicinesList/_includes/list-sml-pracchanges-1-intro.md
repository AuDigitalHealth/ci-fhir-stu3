#### List of Medicine Items with Change Information Authored by Practitioner *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

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

* will be sent with all medicine items considered relevant by the practitioner (source), including packed, non-packed, complementary and over the counter medicine items
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
        <td>recommended medicine item</td>
        <td>Will be represented with the flag of ‘new-recommended’, ‘prescription-recommended’ and a change description that describes the reason to recommend introducing the medicine item</td>
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
        <td>existing medicine item with changes recommended</td>
        <td>Will be represented with the flag of ‘review-recommended’ and a change description that describes the recommended change, e.g. dose, form, route, frequency change</td>
    </tr>
    <tr>
        <td>ceased medicine item</td>
        <td>Will be represented with the flag of ‘ceased’ and a change description that describes the reason for ceasing the medicine item</td>
    </tr>
    <tr>
        <td>withheld medicine item</td>
        <td>Will be represented with the flag of ‘suspended’ and a change description supplied that describes reason for withholding the medicine, expected restart date or request for a clinical review</td>
    </tr>
    <tr>
        <td>existing medicine item with stop recommended</td>
        <td>Will be represented with the flag of ‘cessation-recommended’, ‘suspension-recommended’ or ‘cancellation-recommended’ and a change description that describes the reason for stopping the medicine item</td>
    </tr>
    </table>
When sending a shared medicines list to the My Health Record system it is expected that all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).

When a shared medicines list is sent as part of a document, rather than as a standalone resource, the guidance in the following table applies.

<table class="list" width="100%">
  <tr>
    <th>List element</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>author-role</td>
        <td>Will be sent with the same PractitionerRole as Composition.composition-author-role</td>
    </tr>
   <tr>
        <td>code</td>
        <td>Will be sent with the same code as Composition.section(medications).code</td>
   </tr>   
   <tr>
        <td>subject</td>
        <td>Will be sent with the same Patient as Composition.subject</td>
    </tr>   
   <tr>
        <td>date</td>
        <td>Will be sent with the same datetime as Composition.date</td>
    </tr>   
   <tr>
        <td>source</td>
        <td>Will be sent with the same Practitioner as Composition.author</td>
    </tr>    
       <tr>
        <td>title</td>
        <td>Will not be sent</td>
    </tr>  
  </table> 

Additionally, when the shared medicines list is a PSML document it is expected that:

* if the list has a List.code of '10160–0' History of Medication use Narrative, it will be sent with at least one new or existing medicine item
* encounter will be sent
* when sending flag, the codes from [Medicine Item Change from Practitioner Medicine Review](https://healthterminologies.gov.au/fhir/ValueSet/medicine-item-change-from-practitioner-medicines-review-1) are expected
* list items will not include recommended medicine items, existing medicine items with changes recommended, existing medicine item with stop recommended, or new prescribed medicine items (flag is not to be ‘prescribed’)
* packed-in-daa-1 will be sent

This profile is referenced by [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html).