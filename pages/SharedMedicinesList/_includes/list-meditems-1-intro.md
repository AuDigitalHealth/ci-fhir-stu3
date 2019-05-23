### List of Medicine Items for a Patient *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

* A medicine list exchanged as a standalone record

* A medicine list exchanged as a referenced entry in a Composition
 
Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.

#### Implementation guidance

For the expected usage scenarios in this implementation guide:
* Related prescription and dispense records can be included via referenced medication statement

* When list is used in Composition
<table class="list" width="100%">
  <tr>
    <th>Element</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>list source role</td>
        <td>Expected to be the same as the authoring role of the referencing Composition</td>
    </tr>
   <tr>
        <td>subject</td>
        <td>Expected to be the same as the subject of the referencing Composition</td>
    </tr>   
   <tr>
        <td>date</td>
        <td>Expected to be the same as the date of the referencing Composition</td>
    </tr>   
   <tr>
        <td>source</td>
        <td>Expected to be the same as the author of the referencing Composition</td>
    </tr>    
       <tr>
        <td>title</td>
        <td>Not expected to be provided</td>
    </tr>  
  </table> 


* PSML implementation guidance

 * The list should have at least one entry.
 * All medicines that the patient is known to be taking, including packed, non-packed, complementary and over the counter medicine items, should be included in the list.
 * Relevant ceased medicine items for the patient may be included in the list.
 * A new medicine item should be represented with the flag of 'new' or 'prescribed' and a change description that described the reason for introducing the medicine item.
 * An existing unchanged medicine item should be represented with the flag of 'nochange' and no change description.
 * A changed medicine item should be represented with the flag of 'amended' and a change description that describes the change, e.g. dose, form, route, frequency change.
 * A ceased medicine item should be represented with the flag of 'ceased' and a change description that describes the reason for ceasing the medicine item.
 * A withheld medicine item should be represented with the flag of 'suspended' and a change-description supplied that describes reason for withholding the medicine, expected restart date or request for a clinical review.


