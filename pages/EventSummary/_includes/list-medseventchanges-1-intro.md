#### List of Medicine Changes from an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

* A medicine list exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* all medicine items relevant to an event should be included in the list
* all medicine items will have an associated flag according to the guidance in the following table

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
When sending a medicines list to the My Health Record system it is expected that all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).

When a medicines list is sent as part of a document, rather than as a standalone resource, the guidance in the following table applies.

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

This profile is referenced by [Event Summary](StructureDefinition-composition-es-1.html)
