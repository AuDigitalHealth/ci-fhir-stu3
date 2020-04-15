#### Advance Care Planning Document Reference *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage Scenarios
The following are the overarching usage scenarios this profile is intended to support:
* A clinical information system (CIS) sends or receives an advance care planning document reference with the My Health Record system
* A contracted service provider (CSP) sends or receives an advance care planning document reference with the My Health Record system
* A CIS sends or receives an advance care planning document reference with another CIS or CSP
* A CSP sends or receives an advance care planning document reference with a CIS or another CSP
* A registered portal or registered repository receives an advance care planning document reference
 
An expected usage scenario, further scoping the above overarching scenarios is:
* An advance care planning document reference exchanged as goals of care document

A system may be a producer by attaching the Advance Care Plan document to the Document Reference and sending that Document Reference.

#### Implementation guidance
When an advance care planning document reference is sent as part of a document, rather than as a standalone resource, the guidance in the following table applies.
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
        <td>subject</td>
        <td>Will be sent with the same Patient as Composition.subject</td>
    </tr>   
   <tr>
        <td>author</td>
        <td>Will be sent with the same Practitioner as Composition.author</td>
    </tr>    
  </table> 
 
When sending to the My Health Record system it is expected that:
* all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).
* the document in content.attachment will be sent as a PDF

Additionally, when the document that is referenced is a goals of care document it is expected that type will be "100.32016" Goals of Care.

This profile is referenced by [Advance Care Planning](StructureDefinition-composition-acp-1.html).

