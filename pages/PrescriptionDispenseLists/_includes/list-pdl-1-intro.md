#### List of Prescription and or Dispense Records *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
The following are the overarching usage scenarios this profile is intended to support:
* A clinical information system (CIS) sends or receives
  * a prescription list with the My Health Record system
  * a dispense record list with the My Health Record system
  * a prescription and dispense record list with the My Health Record system
* A contracted service provider (CSP) sends or receives
   * a prescription list with the My Health Record system
   * a dispense record list with the My Health Record system
   * a prescription and dispense record list with the My Health Record system
* A CIS sends or receives
  * a prescription list with another CIS or CSP
  * a dispense record list with another CIS or CSP
  * a prescription and dispense record list with another CIS or CSP
* A CSP sends or receives
  * a prescription list with a CIS or another CSP
  * a dispense record list with a CIS or another CSP
  * a prescription and dispense record list list with a CIS or another CSP
* A registered portal or registered repository receives
    * a prescription list
    * a dispense record list
    * a prescription and dispense record list 

An expected usage scenario, further scoping the above overarching scenarios is:
* Prescription and dispense view (PDV) exchanged with the My Health Record system

This profile does not support sending medicines change information (e.g. indicating cancellation or newly prescribed items) or event-specific information; in this case it is recommended that information is supplied as a shared medicines list.  

#### Implementation guidance
For the above overarching scenarios in this implementation guide it is expected that:
* the use of MedicationStatement is discouraged
* where possible systems are encouraged to send MedicationDispense or MedicationRequest

When the list is a prescription and dispense view it is expected that:
* the source will be a Device (My Health Record system)
* the date will be the time the PDV is generated

When the list is sent as part of a document (referenced in Composition.section.entry) the following guidance applies:
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
        <td>author-related-person</td>
        <td>Will be sent with the same Relatedperson as Composition.author</td>
    </tr>
   <tr>
        <td>code</td>
        <td>Will be sent with the same code as Composition.section.code</td>
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
        <td>Will be sent with the same resource as Composition.author</td>
    </tr>    
       <tr>
        <td>title</td>
        <td>Will not be sent</td>
    </tr>  
  </table> 

This profile is referenced by [Prescription and / or Dispense List](StructureDefinition-composition-pdl-1.html)